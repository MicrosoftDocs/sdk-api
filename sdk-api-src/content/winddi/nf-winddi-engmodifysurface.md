---
UID: NF:winddi.EngModifySurface
title: EngModifySurface function (winddi.h)
description: The EngModifySurface function notifies GDI about the attributes of a surface that was created by the driver.
helpviewer_keywords: ["EngModifySurface","EngModifySurface function [Display Devices]","display.engmodifysurface","gdifncs_422719a8-bffd-4c92-bbb8-fbd53ee1ce09.xml","winddi/EngModifySurface"]
old-location: display\engmodifysurface.htm
tech.root: display
ms.assetid: 176f51c0-0075-4afb-8b5c-5d0b6b64a3ad
ms.date: 12/05/2018
ms.keywords: EngModifySurface, EngModifySurface function [Display Devices], display.engmodifysurface, gdifncs_422719a8-bffd-4c92-bbb8-fbd53ee1ce09.xml, winddi/EngModifySurface
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
 - EngModifySurface
 - winddi/EngModifySurface
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
 - EngModifySurface
---

# EngModifySurface function


## -description

The <b>EngModifySurface</b> function notifies GDI about the attributes of a surface that was created by the driver.

## -parameters

### -param hsurf

Handle to the surface to be modified. This parameter is the surface handle returned by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatedevicebitmap">EngCreateDeviceBitmap</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engcreatedevicesurface">EngCreateDeviceSurface</a>, or from the <b>hsurf</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure.

### -param hdev

Handle to the device with which the surface is to be associated. This is the handle that GDI passed to <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>.

### -param flHooks

Is a set of flags that control the functions the driver can hook whenever GDI drawing occurs on the specified surface. This can be a bitwise OR of any of the HOOK_<i>Xxx</i> values listed on the <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a> reference page.

### -param flSurface

Is a set of flags that describe the surface's attributes. Currently, the driver should set this to MS_NOTSYSTEMMEMORY when the surface is located in video memory.

### -param dhsurf

Identifies the surface to the driver. The driver can set this to anything; GDI sets the <b>dhsurf</b> member of the resulting surface's <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure to this value if the function is successful.

### -param pvScan0

Pointer to the virtual address of the start of the bitmap.

### -param lDelta

Is the virtual address stride of the bitmap; that is, the number of bytes between the beginning of one bitmap row and the next.

### -param pvReserved

Is reserved and must always be set to <b>NULL</b>.

## -returns

<b>EngModifySurface</b> returns <b>TRUE</b> upon success; otherwise it returns <b>FALSE</b>.

## -remarks

<b>EngModifySurface</b> allows the driver to modify a <a href="/windows-hardware/drivers/">device-managed surface</a> and inform GDI of this surface's attributes. This allows drivers to convert the destination surface from being opaque to nonopaque, thus allowing GDI to draw on the surface.

The DIB engine uses <i>pvScan0</i> and <i>lDelta</i> to draw directly to the surface. When these parameters are <b>NULL</b>, the surface is opaque to GDI, and GDI will revert to calling <a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a> for drawing operations not hooked by the driver.

After <a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a> returns a handle to a primary surface, do not call <b>EngModifySurface</b> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="https://support.microsoft.com/?kbid&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>