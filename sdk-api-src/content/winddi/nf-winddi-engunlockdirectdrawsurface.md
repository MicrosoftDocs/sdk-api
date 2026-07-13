---
UID: NF:winddi.EngUnlockDirectDrawSurface
title: EngUnlockDirectDrawSurface function (winddi.h)
description: The EngUnlockDirectDrawSurface function releases the lock on the specified surface.
helpviewer_keywords: ["EngUnlockDirectDrawSurface","EngUnlockDirectDrawSurface function [Display Devices]","display.engunlockdirectdrawsurface","gdifncs_6582e033-3e56-4a8d-904d-2978c63ddd4b.xml","winddi/EngUnlockDirectDrawSurface"]
old-location: display\engunlockdirectdrawsurface.htm
tech.root: display
ms.assetid: 61d1ff1a-d5e3-4542-953c-8b1771622a63
ms.date: 12/05/2018
ms.keywords: EngUnlockDirectDrawSurface, EngUnlockDirectDrawSurface function [Display Devices], display.engunlockdirectdrawsurface, gdifncs_6582e033-3e56-4a8d-904d-2978c63ddd4b.xml, winddi/EngUnlockDirectDrawSurface
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
 - EngUnlockDirectDrawSurface
 - winddi/EngUnlockDirectDrawSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngUnlockDirectDrawSurface
---

# EngUnlockDirectDrawSurface function


## -description

The <b>EngUnlockDirectDrawSurface</b> function releases the lock on the specified surface.

## -parameters

### -param pSurface [in]

Pointer to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface to be unlocked.

## -returns

<b>EngUnlockDirectDrawSurface</b> returns <b>TRUE</b> when it successfully unlocks the specified surface. Otherwise, it returns <b>FALSE</b>.

## -remarks

The surface must previously have been locked by <a href="/windows/desktop/api/winddi/nf-winddi-englockdirectdrawsurface">EngLockDirectDrawSurface</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-englockdirectdrawsurface">EngLockDirectDrawSurface</a>