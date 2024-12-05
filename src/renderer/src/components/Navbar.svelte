<script>
  let navbarButtons = [
    {
      title: 'Dashboard',
      svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>monitor-dashboard</title><path d="M21,16V4H3V16H21M21,2A2,2 0 0,1 23,4V16A2,2 0 0,1 21,18H14V20H16V22H8V20H10V18H3C1.89,18 1,17.1 1,16V4C1,2.89 1.89,2 3,2H21M5,6H14V11H5V6M15,6H19V8H15V6M19,9V14H15V9H19M5,12H9V14H5V12M10,12H14V14H10V12Z" /></svg>'
    }
  ]

  let dropdownButtons = [
    {
      title: 'Manage',
      svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>chevron-down</title><path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z" /></svg>',
      submenu: [
        {
          subTitle: 'Add Income',
          svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>plus-box</title><path d="M17,13H13V17H11V13H7V11H11V7H13V11H17M19,3H5C3.89,3 3,3.89 3,5V19A2,2 0 0,0 5,21H19A2,2 0 0,0 21,19V5C21,3.89 20.1,3 19,3Z" /></svg>'
        },
        {
          subTitle: 'Add Expense',
          svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>plus-box</title><path d="M17,13H13V17H11V13H7V11H11V7H13V11H17M19,3H5C3.89,3 3,3.89 3,5V19A2,2 0 0,0 5,21H19A2,2 0 0,0 21,19V5C21,3.89 20.1,3 19,3Z" /></svg>'
        }
      ]
    },
    {
      title: 'View',
      svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>chevron-down</title><path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z" /></svg>',
      submenu: [
        {
          subTitle: 'Incomes',
          svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>treasure-chest</title><path d="M5,4H19A3,3 0 0,1 22,7V11H15V10H9V11H2V7A3,3 0 0,1 5,4M11,11H13V13H11V11M2,12H9V13L11,15H13L15,13V12H22V20H2V12Z" /></svg>'
        },
        {
          subTitle: 'Expenses',
          svg: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>treasure-chest</title><path d="M5,4H19A3,3 0 0,1 22,7V11H15V10H9V11H2V7A3,3 0 0,1 5,4M11,11H13V13H11V11M2,12H9V13L11,15H13L15,13V12H22V20H2V12Z" /></svg>'
        }
      ]
    }
  ]
</script>

<nav>
  <ul>
    {#each navbarButtons as { title, svg }}
      <li>
        <button>
          <span>{title}</span>
          {@html svg}
        </button>
      </li>
    {/each}
    {#each dropdownButtons as { title, svg, submenu }}
      <li>
        <button>
          <span>{title}</span>
          {@html svg}
        </button>
        <ul>
          {#each submenu as { subTitle, svg }}
            <li>
              <button>
                <span>{subTitle}</span>
                {@html svg}
              </button>
            </li>
          {/each}
        </ul>
      </li>
    {/each}
  </ul>
</nav>

<style>
  nav {
    position: sticky;
    top: 0;
    height: 100%;
    width: 250px;
    border-right: 1px solid var(--bg-grey-600);
  }
</style>
