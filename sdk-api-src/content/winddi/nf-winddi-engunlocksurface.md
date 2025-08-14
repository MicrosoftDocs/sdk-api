---
UID: NF:winddi.EngUnlockSurface
title: EngUnlockSurface function (winddi.h)
description: The EngUnlockSurface function causes GDI to unlock the surface.
helpviewer_keywords: ["EngUnlockSurface","EngUnlockSurface function [Display Devices]","display.engunlocksurface","gdifncs_a7050a36-0beb-4f7e-857c-5d1e13d5f530.xml","winddi/EngUnlockSurface"]
old-location: display\engunlocksurface.htm
tech.root: display
ms.assetid: 49d089e3-c900-4f81-a6ee-420a5558a4ff
ms.date: 12/05/2018
ms.keywords: EngUnlockSurface, EngUnlockSurface function [Display Devices], display.engunlocksurface, gdifncs_a7050a36-0beb-4f7e-857c-5d1e13d5f530.xml, winddi/EngUnlockSurface
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
 - EngUnlockSurface
 - winddi/EngUnlockSurface
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
 - EngUnlockSurface
---

# EngUnlockSurface function


## -description

The <b>EngUnlockSurface</b> function causes GDI to unlock the surface.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface to be unlocked.

## -returns

None

## -remarks

The specified surface must previously have been locked by a call to <a href="/windows/desktop/api/winddi/nf-winddi-englocksurface">EngLockSurface</a>. The pointer to the SURFOBJ structure must not be used after this call.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-englocksurface">EngLockSurface</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>