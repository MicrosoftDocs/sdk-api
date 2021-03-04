---
description: "MCCS warning"
title: MCCS warning
ms.topic: include
author: zhuman
ms.author: zanor
ms.date: 08/27/2020
ms.localizationpriority: medium
---

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement this standard, and use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.
