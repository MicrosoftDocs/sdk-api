---
UID: NF:winddi.EngCreateDeviceBitmap
title: EngCreateDeviceBitmap function (winddi.h)
description: The EngCreateDeviceBitmap function requests GDI to create a handle for a device bitmap.
helpviewer_keywords: ["EngCreateDeviceBitmap","EngCreateDeviceBitmap function [Display Devices]","display.engcreatedevicebitmap","gdifncs_e802b5e9-a939-4aa4-b4df-82172e825fa5.xml","winddi/EngCreateDeviceBitmap"]
old-location: display\engcreatedevicebitmap.htm
tech.root: display
ms.assetid: dc9d7154-30b9-4462-9161-6df03946308d
ms.date: 12/05/2018
ms.keywords: EngCreateDeviceBitmap, EngCreateDeviceBitmap function [Display Devices], display.engcreatedevicebitmap, gdifncs_e802b5e9-a939-4aa4-b4df-82172e825fa5.xml, winddi/EngCreateDeviceBitmap
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
 - EngCreateDeviceBitmap
 - winddi/EngCreateDeviceBitmap
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
 - EngCreateDeviceBitmap
---

# EngCreateDeviceBitmap function


## -description

The <b>EngCreateDeviceBitmap</b> function requests GDI to create a handle for a device bitmap.

## -parameters

### -param dhsurf [in]

Device handle to the device bitmap to be created.

### -param sizl [in]

Specifies a SIZEL structure that contains the width and height of the bitmap to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the bitmap's width and height, in pixels. A SIZEL structure is identical to a <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -param iFormatCompat

Specifies the compatible engine format of the device surface being created. This is used by GDI if a temporary buffer is needed to simulate a complicated drawing call. The allowable values for <i>iFormatCompat</i> are BMF_1BPP, BMF_4BPP, BMF_8BPP, BMF_16BPP, BMF_24BPP, and BMF_32BPP.

## -returns

The return value is a handle that identifies the bitmap if the function is successful. Otherwise, it is zero, and an error code is logged.

## -remarks

The surface should be associated by using <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>. The bitmap should be deleted by calling <a href="/windows/desktop/api/winddi/nf-winddi-engdeletesurface">EngDeleteSurface</a> when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>