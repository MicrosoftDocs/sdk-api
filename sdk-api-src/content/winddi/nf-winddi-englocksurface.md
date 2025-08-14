---
UID: NF:winddi.EngLockSurface
title: EngLockSurface function (winddi.h)
description: The EngLockSurface function creates a user object for a given surface. This function gives drivers access to surfaces they create.
helpviewer_keywords: ["EngLockSurface","EngLockSurface function [Display Devices]","display.englocksurface","gdifncs_99ca0d6a-a445-42ad-96fb-4ef8d3e23db7.xml","winddi/EngLockSurface"]
old-location: display\englocksurface.htm
tech.root: display
ms.assetid: a5d44e16-459c-4722-b3e8-5dc4b5be5865
ms.date: 12/05/2018
ms.keywords: EngLockSurface, EngLockSurface function [Display Devices], display.englocksurface, gdifncs_99ca0d6a-a445-42ad-96fb-4ef8d3e23db7.xml, winddi/EngLockSurface
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngLockSurface
 - winddi/EngLockSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngLockSurface
---

# EngLockSurface function


## -description

The <b>EngLockSurface</b> function creates a user object for a given surface. This function gives drivers access to surfaces they create.

## -parameters

### -param hsurf

Handle to the surface to be locked.

## -returns

<b>EngLockSurface</b> returns a pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure if the function is successful. Otherwise, this function returns <b>NULL</b>.

## -remarks

This function gives drivers access to surfaces they create.

The driver is responsible for unlocking the surface when it no longer needs it. Surfaces should be locked only for very short periods of time.

Use the <a href="/windows/desktop/api/winddi/nf-winddi-engunlocksurface">EngUnlockSurface</a> function to unlock the surface.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engunlocksurface">EngUnlockSurface</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>