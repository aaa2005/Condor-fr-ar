# Condor-fr-ar

Custom XKB keyboard layouts for **Condor CBook CL-502** laptops running Linux.

This project provides custom keyboard layouts that correctly match the physical keyboard found on newer Condor CBook CL-502 laptops, whose layout is not available in the default Linux XKB database.

## Included layouts

* **Condor French ANSI**
* **Condor Arabic ANSI**

Both layouts are designed to match the physical key positions of the laptop keyboard.

## Tested on

* Fedora Workstation (GNOME / Wayland)
* XKB-based desktop environments

Other Linux distributions using XKB should also work.

---

## Installation

### 1. Copy the layout files

Copy the provided symbol files into the XKB symbols directory.

```bash
sudo cp symbols/condor /usr/share/X11/xkb/symbols/
sudo cp symbols/condor-ara /usr/share/X11/xkb/symbols/
```

### 2. Register the layouts

Copy the provided XKB rule files or manually merge the changes into:

```
/usr/share/X11/xkb/rules/evdev.xml
/usr/share/X11/xkb/rules/evdev.lst
```

If your distribution also uses `base.xml` and `base.lst`, apply the same changes there.

### 3. Clear the XKB cache

```bash
sudo rm -rf /var/lib/xkb/*
```

### 4. Log out and back in

Or reboot your computer.

### 5. Add the layouts

Open:

**Settings → Keyboard → Input Sources**

Add one of the following:

* Condor French ANSI
* Condor Arabic ANSI

---



## Repository Structure

```
.
├── symbols/
│   ├── condor
│   └── condor-ara
├── rules/
│   ├── evdev.xml
│   └── evdev.lst
└── README.md
```

---

## Notes

* This project is intended for the physical keyboard used on the **Condor CBook CL-502**.
* Other Condor models may use different keyboard hardware and may require different mappings.
* These layouts use the Linux XKB system and are compatible with modern desktop environments that support XKB.

## License

MIT License
