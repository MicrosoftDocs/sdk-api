---
UID: NF:winddi.EngLockDirectDrawSurface
title: EngLockDirectDrawSurface function (winddi.h)
description: The EngLockDirectDrawSurface function locks the kernel-mode handle of a DirectDraw surface.
helpviewer_keywords: ["EngLockDirectDrawSurface","EngLockDirectDrawSurface function [Display Devices]","display.englockdirectdrawsurface","gdifncs_f0027001-42bd-4f64-b5c0-c7ec3768f72c.xml","winddi/EngLockDirectDrawSurface"]
old-location: display\englockdirectdrawsurface.htm
tech.root: display
ms.assetid: be43afe9-97c9-4ae4-b18c-3312ae757798
ms.date: 12/05/2018
ms.keywords: EngLockDirectDrawSurface, EngLockDirectDrawSurface function [Display Devices], display.englockdirectdrawsurface, gdifncs_f0027001-42bd-4f64-b5c0-c7ec3768f72c.xml, winddi/EngLockDirectDrawSurface
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
 - EngLockDirectDrawSurface
 - winddi/EngLockDirectDrawSurface
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
 - EngLockDirectDrawSurface
---

# EngLockDirectDrawSurface function


## -description

The <b>EngLockDirectDrawSurface</b> function locks the kernel-mode handle of a DirectDraw surface.

## -parameters

### -param hSurface [in]

Handle to the surface to be locked.

## -returns

<b>EngLockDirectDrawSurface</b> returns a pointer to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface information upon success. Otherwise, it returns a <b>NULL</b> pointer.

## -remarks

<b>EngLockDirectDrawSurface</b> allows driver writers to lock DirectDraw surfaces. Locking the handle guarantees synchronized behavior and preserves the handle from being deleted by other threads in the system.

Currently, the driver receives DirectDraw surface handles only from the Direct3D texturing interface. Consequently, only drivers that perform texturing need to lock texture surfaces.

Upon completion of texturing, the driver must release the locked handle by calling <a href="/windows/desktop/api/winddi/nf-winddi-engunlockdirectdrawsurface">EngUnlockDirectDrawSurface</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engunlockdirectdrawsurface">EngUnlockDirectDrawSurface</a>