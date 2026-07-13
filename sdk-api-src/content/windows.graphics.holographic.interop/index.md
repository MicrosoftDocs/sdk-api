---
UID: NA:windows.graphics.holographic.interop
title: Windows.Graphics.Holographic.Interop.h header
ms.author: windowssdkdev
ms.date: 12/12/2019
ms.keywords: 
ms.service: windows
ms.subservice: windows
ms.topic: overview
ms.update-cycle: 1095-days
tech.root: direct3d12
f1_keywords:
 - windows.graphics.holographic.interop
 - windows.graphics.holographic.interop/windows.graphics.holographic.interop
---

# Windows.Graphics.Holographic.Interop.h header


## -description

The APIs in the `Windows.Graphics.Holographic.Interop.h` header allow Windows Mixed Reality apps to use Direct3D 12. The interfaces specified in this header use COM interface pointers to pass DirectX COM objects as parameters to methods on Windows Runtime objects in the [Windows.Graphics.Holographic](/uwp/api/windows.graphics.holographic) namespace, allowing Windows Mixed Reality apps to create and use Direct3D 12 buffer resources with no additional overhead.

Sample code for this API set is included in the [Windows Mixed Reality Direct3D 12 app template](https://marketplace.visualstudio.com/items?itemName=WindowsMixedRealityteam.WindowsMixedRealityAppTemplatesVSIX). The Windows Mixed Reality Direct3D 12 app template includes boilerplate code for most APIs that are provided in the `Windows.Graphics.Holographic.Interop.h` header, and renders a spinning cube on a Windows Mixed Reality PC, a HoloLens 2, and the HoloLens 2 emulator.

This header is used by Direct3D 12 Graphics. For more information, see:

- [Direct3D 12 Graphics](../_direct3d12/index.md)

