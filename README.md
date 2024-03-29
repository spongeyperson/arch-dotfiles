# <p align=center>- Spongey's Arch Linux KDE Dotfiles -
###### <p align=center> A Simple Git Repository to store various Arch Linux User Configs (Dotfiles).

<p align=center><img src="https://user-images.githubusercontent.com/28176188/210040764-90bf0b89-1e4f-4f6f-aa42-35a006060849.png" title="I Run Arch Btw"></p>

<h2>Index:</h2>
<ul>
  <li><b>This Repo</b>:</li>
  <ul>
    <li><a href="#cloning-this-repo">Cloning this Repo</a></li>
    <li><b><u>Branches:</u></b></li>
      <ul>
        <li><a href="https://github.com/spongeyperson/arch-dotfiles/tree/unused">Unused files Branch</a></li>
      </ul>   
      <li><b><u>Configurations</u></b>:</li>
        <ul>
          <li><a href="./etc/X11/xorg.conf.d/">Xorg configuration</a></li>
          <li><a href="./home/tyler/.local/share/plasma/layout-templates">Custom KDE panels</a></li>
          <li><b><u>VFIO / GPU Passthrough Related</u></b>:</li>
            <ul>
              <li><a href="./usr/share/kvm">GPU VBIOS ROMs</a></li>
              <li><a href="./etc/libvirt/qemu">Virsh Config XMLs</a></li>
            </ul>
          </ul>
        </ul>
      </ul>
    </ul>
  </ul>
</ul>
<li><b>Other Repos</b>:</li>
  <ul>
  <li><b>Extra Dotfiles, Belonging to this Repo:</b> <a href="../../../dotfiles-extras"><sup><code>../dotfiles-extras</code></sup></a></li>
    <ul>
      <li><b><u>Documentation:</u></b></li>
      <ul>
        <li><a href="../../../dotfiles-extras/blob/main/docs/PRIME-Render-Settings.md">(WIP) Prime Render Offload Settings:</a></li>
        <li><img src="https://user-images.githubusercontent.com/28176188/224575749-b843d685-2e1e-43bc-8267-ee337fde8206.svg" width="14" height="14"><b> <u>Wine Related:</b></u></li>
        <ul>
          <li><a href="../../../dotfiles-extras/blob/main/docs/Game-Settings.md">Game settings<a></li>
          <li><a href="../../../dotfiles-extras/blob/main/docs/Game-Troubleshooting.md">Game troubleshooting<a></li>
        </ul>
        <li><b><u>Hardware Specific Fixes & Settings:</u></b></li>
          <ul>
            <li><a href="../../../dotfiles-extras/blob/main/docs/Hardware%20Specific%20Fixes%20%26%20Settings/Steam%20Deck%20Settings.md">Steam Deck</a></li>
            <li><a href="../../../dotfiles-extras/blob/main/docs/Hardware%20Specific%20Fixes%20%26%20Settings/ROG-G15-config.md">ROG G15 AMD Advantage on Linux</a></li>
            <li><a href="../../../dotfiles-extras/blob/main/docs/Hardware%20Specific%20Fixes%20%26%20Settings/ZENITH-II-Extreme-config.md">(WIP) TRX40 Zenith II Extreme on Linux</a></li>
          </ul>
      </ul>
      <li><b><u>Configurations</u></b>:</li>
        <ul>
          <li><a href="../../../dotfiles-extras/tree/main/virshxml_examples">Virsh Config XML Examples</a></li>
        </ul>
    </ul>
  </ul>
</ul>
<ul>
  <li><b>Other Dotfiles</b>:</li>
    <ul>
      <li><b>Fedora (ROG G15)</b>: <a href="../../../fedora-dotfiles-laptop/">spongeyperson/fedora-dotfiles-laptop</a></li>
      <li><b>Fedora</b>: <a href="../../../fedora-dotfiles/">spongeyperson/fedora-dotfiles</a></li>
      <li><b>Proxmox</b>: <a href="../../../proxmox-config/">spongeyperson/proxmox-config</a></li>
    </ul>
  </ul>
</ul>

## Cloning this Repo:
> Please note, this information was taken from the following source and changed to fit the content of this repo.
> https://www.atlassian.com/git/tutorials/dotfiles


### From Scratch:

  1) <b>Initialize the Repo:</b>
      ```bash
      git init --bare $HOME/.dotfiles
      ```
  2) <b>Set an Alias in your Shell's Config:</b>
      > Fish Shell:
      ```bash
      echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=/'" >> $HOME/.config/fish/config.fish
      ```
      > Bash Shell:
      ```bash
      echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=/'" >> $HOME/.bashrc
      ```
  3) <b>Globally Untrack Files that aren't part of the Dotfiles</b>
      ```bash
      dotfiles config --local status.showUntrackedFiles no
      ```

### Migrate / Merge into System:

  1) <b>Set an Alias in your Shell's Config:</b>
      > Fish Shell:
      ```bash
      echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=/'" >> $HOME/.config/fish/config.fish
      ```
      > Bash Shell:
      ```bash
      echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=/'" >> $HOME/.bashrc
      ```
  2) <b>Globally Untrack Files that aren't part of the Dotfiles</b>
      ```bash
      dotfiles config --local status.showUntrackedFiles no
      ```
  3) <b>Set Dotfiles Repo Source as ignored:</b>
      ```bash
      echo ".dotfiles" >> .gitignore
      ```
  4) <b>Clone Bare Repo:</b>
      ```bash
      git clone --bare https://github.com/spongeyperson/arch-dotfiles.git $HOME/.dotfiles/
      ```
  5) <b>Checkout Content from Remote Repo:</b>
      ```bash
      dotfiles checkout
      ```


---
###### <p align=center> Note: I do <ins>not</ins> pretend to own any content on this git repository. All contents are copyright of their respective owners. This repository is intented for recreating Linux installs only. Content on this repository is installed <ins>at your own risk</ins>. If you have any legal issue with the content on this repository, please make a github issue and i will create a submodule linking to your project instead.</p>
