<html>
<body>
<div class="container">
<h1>
  Salt 16 Debian Repository
</h1>
<h3>
  Location
</h3>
<ul>
  <li>
    <a href="https://goodwillcoding.github.io/salt16-debian-repository">https://goodwillcoding.github.io/salt16-debian-repository</a>
  </li>
</ul>
<h3>
  Supported Distributions
</h3>
<ul>
  <li>
    Xenial
  </li>
</ul>

<h3>
  Adding this repository as an APT source
</h3>
<ol>
  <li>
    Launch your terminal application (Terminal, Console, iTerm2, etc...)
    <blockquote>
      ...
    </blockquote>
  </li>
  <li>
    Find out youy distribution by running the following command in your
    terminal.
    <blockquote>
      <pre>lsb_release --short --codename</pre>
      You will see your distribution (for example, on my system it shows
      <strong>xenial</strong>):
      <blockquote><pre>xenial</pre></blockquote>
    </blockquote>
  </li>
  <li>
    <p>
      Add the repository for your distribution (from the last command) to your
      APT sources by running the following command in your terminal.
    </p>
    <blockquote>
    <div class='panel panel-default'>
      <div class="panel-heading">
        For the <strong>Xenial</strong> distribution run:
      </div>
      <div class="panel-body">
        <pre>echo "deb https://goodwillcoding.github.io/salt16-debian-repository xenial main #Salt 16 Debian Repository" \
| sudo tee --append /etc/apt/sources.d/salt16-xenial.list</pre>
      </div>
    </div>
    </blockquote>
  </li>
  <li>
    <p>
      Import the Salt 16 Debian Repository <strong>Public GPG key</strong>
      (which was used to sign with repository) by running the following command
      in your terminal.
    </p>
    <blockquote>
      <pre>wget --quiet https://goodwillcoding.github.io/salt16-debian-repository/public.asc --output-document - \
| sudo apt-key add -</pre>
    </blockquote>
  </li>
  <li>
    <p>
      Now refresh your local repository index by running the following command
      in your terminal.
    </p>
    <blockquote>
        <pre>sudo apt-get update</pre>
    </blockquote>
  </li>
  <li>
    <p>
      The packages from this repository should now be available for
      installation. You can install any of them by running following command(s)
      in your terminal.
    </p>
    <blockquote>
      To install <strong>salt-master</strong> package run:
      <pre>sudo apt-get install salt-master</pre>
      To install <strong>salt-minion</strong> package run:
      <pre>sudo apt-get install salt-minion</pre>
    </blockquote>
  </li>
</ol>
  <hr />
  <div class="pull-right">
    Repository created on: 2016-12-31 01:41 PST -0800
  </div>
</div>
</body>
</html>
