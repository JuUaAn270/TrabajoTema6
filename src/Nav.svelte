<script>
  import { Link } from "svelte-routing";
</script>

<nav>
  <ul class="menu">
    <li class="logo">
      <Link to="/">
        <span class="inicio">๐</span>
      </Link>
    </li>
    <li class="item active">
      <Link to="/zapatos">
        <span class="zapatos">๐</span>
      </Link>
    </li>
    <li class="item active">
      <Link to="/empleados">
        <span class="empleados">๐ง๐ป</span>
      </Link>
    </li>
  </ul>
</nav>

<style>
  /* Basic styling */
  * {
    box-sizing: border-box;
  }

  nav {
    background: #504e4e;
    padding: 8px;
    position: -webkit-sticky; /* Safari */
    position: sticky;
    top: 0;
    width: 100%;
  }

  ul {
    list-style-type: none;
  }

  span {
    padding-right: 10px;
  }

  .menu li:hover {
    text-shadow: 3px 3px 4px #6f6f70;
  }

  .menu li {
    font-weight: bold;
    font-size: 16px;
    padding: 15px 15px;
    white-space: nowrap;
  }

  /* Mรณvil */
  .menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    flex: 1;
  }
  .item {
    order: 1;
    display: block;
    width: auto;
  }
  .active {
    display: block;
  }
  /* Tablet */
  @media all and (min-width: 600px) {
    .menu {
      justify-content: space-between;
    }
    .logo {
      flex: 1;
    }
    .item {
      order: 1;
      display: block;
      width: auto;
    }

    .inicio::after,
    .zapatos::after,
    .empleados::after {
      display: inline-block;
      padding-left: 10px;
    }

    .inicio::after {
      content: "Inicio";
    }
    .zapatos::after {
      content: "Zapatos";
    }
    .empleados::after {
      content: "Empleados";
    }
  }
  /* PC */
  @media all and (min-width: 900px) {
    .item {
      order: 1;
      display: block;
      width: auto;
    }
    .logo {
      order: 0;
    }
    .menu li {
      padding: 15px 10px;
    }
  }
</style>
