<template>
  <div class="wrapper">
    <!-- Navbar -->
    <nav class="main-header navbar navbar-expand navbar-white navbar-light">
      <!-- Left navbar links -->
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" data-widget="pushmenu" href="#" role="button">
            <i class="fas fa-bars"></i>
          </a>
        </li>
        <li class="nav-item d-none d-sm-inline-block">
          <router-link to="/" class="nav-link">Home</router-link>
        </li>
        <li class="nav-item d-none d-sm-inline-block">
          <a href="#" class="nav-link">Contact</a>
        </li>
      </ul>

      <!-- Right navbar links -->
      <ul class="navbar-nav ml-auto">
        <!-- Navbar Search -->
        <li class="nav-item">
          <a class="nav-link" data-widget="navbar-search" href="#" role="button">
            <i class="fas fa-search"></i>
          </a>
          <div class="navbar-search-block">
            <form class="form-inline">
              <div class="input-group input-group-sm">
                <input class="form-control form-control-navbar" type="search" placeholder="Search" aria-label="Search">
                <div class="input-group-append">
                  <button class="btn btn-navbar" type="submit">
                    <i class="fas fa-search"></i>
                  </button>
                  <button class="btn btn-navbar" type="button" data-widget="navbar-search">
                    <i class="fas fa-times"></i>
                  </button>
                </div>
              </div>
            </form>
          </div>
        </li>
      </ul>
    </nav>
    <!-- /.navbar -->

    <!-- Main Sidebar Container -->
    <aside class="main-sidebar sidebar-dark-primary elevation-4">
      <!-- Brand Logo -->
      <a href="/" class="brand-link">
        <img src="../assets/AdminLTELogo.png" alt="AdminLTE Logo" class="brand-image img-circle elevation-3" style="opacity: .8">
        <span class="brand-text font-weight-light">AdminLTE 3</span>
      </a>

      <!-- Sidebar -->
      <div class="sidebar">
        <!-- Sidebar user panel (optional) -->
        <div class="user-panel mt-3 pb-3 mb-3 d-flex">
          <div class="image">
            <img src="../assets/user2-160x160.jpg" class="img-circle elevation-2" alt="User Image">
          </div>
          <div class="info">
            <a href="#" class="d-block">Admin User</a>
          </div>
        </div>

        <!-- Sidebar Menu -->
        <nav class="mt-2">
          <ul class="nav nav-pills nav-sidebar flex-column" data-widget="treeview" role="menu" data-accordion="false">
            <li class="nav-item">
              <router-link to="/" class="nav-link" :class="{ active: $route.path === '/' }">
                <i class="nav-icon fas fa-tachometer-alt"></i>
                <p>Dashboard</p>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link to="/widgets" class="nav-link" :class="{ active: $route.path === '/widgets' }">
                <i class="nav-icon fas fa-th"></i>
                <p>Widgets</p>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link to="/charts" class="nav-link" :class="{ active: $route.path === '/charts' }">
                <i class="nav-icon fas fa-chart-pie"></i>
                <p>Charts</p>
              </router-link>
            </li>
            
            <!-- Forms Menu -->
            <li class="nav-item" :class="{ 'menu-open': $route.path.startsWith('/forms') }">
              <a href="#" class="nav-link" :class="{ active: $route.path.startsWith('/forms') }">
                <i class="nav-icon fas fa-edit"></i>
                <p>
                  Forms
                  <i class="fas fa-angle-left right"></i>
                </p>
              </a>
              <ul class="nav nav-treeview">
                <li class="nav-item">
                  <router-link to="/forms/general" class="nav-link" :class="{ active: $route.path === '/forms/general' }">
                    <i class="far fa-circle nav-icon"></i>
                    <p>General Elements</p>
                  </router-link>
                </li>
                <li class="nav-item">
                  <router-link to="/forms/advanced" class="nav-link" :class="{ active: $route.path === '/forms/advanced' }">
                    <i class="far fa-circle nav-icon"></i>
                    <p>Advanced Elements</p>
                  </router-link>
                </li>
                <li class="nav-item">
                  <router-link to="/forms/validation" class="nav-link" :class="{ active: $route.path === '/forms/validation' }">
                    <i class="far fa-circle nav-icon"></i>
                    <p>Validation</p>
                  </router-link>
                </li>
              </ul>
            </li>

            <!-- Tables Menu -->
            <li class="nav-item" :class="{ 'menu-open': $route.path.startsWith('/tables') }">
              <a href="#" class="nav-link" :class="{ active: $route.path.startsWith('/tables') }">
                <i class="nav-icon fas fa-table"></i>
                <p>
                  Tables
                  <i class="fas fa-angle-left right"></i>
                </p>
              </a>
              <ul class="nav nav-treeview">
                <li class="nav-item">
                  <router-link to="/tables/simple" class="nav-link" :class="{ active: $route.path === '/tables/simple' }">
                    <i class="far fa-circle nav-icon"></i>
                    <p>Simple Tables</p>
                  </router-link>
                </li>
              </ul>
            </li>

            <!-- Calendar -->
            <li class="nav-item">
              <router-link to="/calendar" class="nav-link" :class="{ active: $route.path === '/calendar' }">
                <i class="nav-icon far fa-calendar-alt"></i>
                <p>Calendar</p>
              </router-link>
            </li>

            <!-- Gallery -->
            <li class="nav-item">
              <router-link to="/gallery" class="nav-link" :class="{ active: $route.path === '/gallery' }">
                <i class="nav-icon far fa-image"></i>
                <p>Gallery</p>
              </router-link>
            </li>

            <!-- Examples Menu -->
            <li class="nav-item" :class="{ 'menu-open': $route.path.startsWith('/examples') }">
              <a href="#" class="nav-link" :class="{ active: $route.path.startsWith('/examples') }">
                <i class="nav-icon fas fa-book"></i>
                <p>
                  Examples
                  <i class="fas fa-angle-left right"></i>
                </p>
              </a>
              <ul class="nav nav-treeview">
                <li class="nav-item">
                  <router-link to="/examples/profile" class="nav-link" :class="{ active: $route.path === '/examples/profile' }">
                    <i class="far fa-circle nav-icon"></i>
                    <p>Profile</p>
                  </router-link>
                </li>
                <li class="nav-item">
                  <router-link to="/examples/invoice" class="nav-link" :class="{ active: $route.path === '/examples/invoice' }">
                    <i class="far fa-circle nav-icon"></i>
                    <p>Invoice</p>
                  </router-link>
                </li>
              </ul>
            </li>
          </ul>
        </nav>
        <!-- /.sidebar-menu -->
      </div>
      <!-- /.sidebar -->
    </aside>

    <!-- Router View - Each page has its own content-wrapper -->
    <router-view></router-view>

    <!-- Main Footer -->
    <footer class="main-footer">
      <strong>Copyright &copy; 2023 <a href="https://adminlte.io">AdminLTE.io</a>.</strong>
      All rights reserved.
      <div class="float-right d-none d-sm-inline-block">
        <b>Version</b> 3.2.0
      </div>
    </footer>
  </div>
  <!-- ./wrapper -->
</template>

<script>
export default {
  name: 'MainLayout',
  mounted() {
    // Initialize AdminLTE
    if (window.AdminLTE) {
      window.AdminLTE.init()
    }
  }
}
</script>

<style scoped>
/* Additional styles can be added here */
</style>
