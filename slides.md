# Rootless Containers

---

* Introduction
* Containers..?
* Rootless containers
  * Why
  * How

---

<!-- .slide: data-background-image="img/containers3.jpg" -->

---

<!-- .slide: data-background-image="img/boxes.jpg" -->

---

# Kernel Features

---

# Namespaces

Isolated view of system resources

---

* Mount (mnt)
* Process ID (pid)
* Network (net)
* Interprocess communication (ipc)
* **User ID (user)**
* ...

---

# CGroups

Limited access to shared system resources

---

``` sh
# Example: set the maximum memory limit to 100MB
mkdir /sys/fs/cgroup/memory/<CGRP>
echo 100000000 > /sys/fs/cgroup/memory/<CGRP>/memory.limit_in_bytes
echo <PID> > /sys/fs/cgroup/memory/<CGRP>/cgroup.procs
```

---

<!-- .slide: data-background-image="img/ship.jpg" -->

---

# Manifest

---

# Runtime

---

<img src="img/oci.png" class="plain">

runc

---

# Rootless

---

Allow an unprivileged user to:

* Create, run, and manage containers.
* Create, modify, distribute, and extract container images.

---

# Why Rootless

---

## Python 3 vs. Python 2

---

## Layers of Security

---

blog.jessfraz.com/post/ultimate-linux-on-the-desktop

---

# How

---

namespaces / <del>cgroups</del>

---

# user namespaces

Make the contained process think it is PID 1

---

## `runc` emulates certain system calls

`setgroups`, `chown`, ...

---

## capabilities

---

## seccomp

---

## Creating and distributing containers

umoci

skopeo

---

# Done?

rootlesscontaine.rs

Rootless Containers with runC - Aleksa Sarai, SUSE

The Route to Rootless Containers - Claudia Beresford & Ed King, Pivotal

---

<!-- .slide: data-background="#02D35F" -->

SUSE Containers as a Service Platform

SUSE Cloud Application Platform

SUSE OpenStack Cloud

SUSE Linux High Availability

**suse.com/careers**
