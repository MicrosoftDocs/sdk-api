---
UID: NF:winddi.EngCreateDeviceSurface
title: EngCreateDeviceSurface function (winddi.h)
description: The EngCreateDeviceSurface function creates and returns a handle for a device surface that the driver will manage.
helpviewer_keywords: ["EngCreateDeviceSurface","EngCreateDeviceSurface function [Display Devices]","display.engcreatedevicesurface","gdifncs_0a48d849-3e93-4310-87e1-cd0b6882b4a4.xml","winddi/EngCreateDeviceSurface"]
old-location: display\engcreatedevicesurface.htm
tech.root: display
ms.assetid: 9c3ca4c4-7614-4739-8333-202c6ec2eab8
ms.date: 12/05/2018
ms.keywords: EngCreateDeviceSurface, EngCreateDeviceSurface function [Display Devices], display.engcreatedevicesurface, gdifncs_0a48d849-3e93-4310-87e1-cd0b6882b4a4.xml, winddi/EngCreateDeviceSurface
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
 - EngCreateDeviceSurface
 - winddi/EngCreateDeviceSurface
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
 - EngCreateDeviceSurface
---

# EngCreateDeviceSurface function


## -description

The <b>EngCreateDeviceSurface</b> function creates and returns a handle for a device surface that the driver will manage.

## -parameters

### -param dhsurf [in]

Device handle to the surface to be managed by the device. This handle is passed to the driver when a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure is passed for input or output.

### -param sizl [in]

Specifies a SIZEL structure that contains the width and height of the surface to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the surface's width and height, in pixels. A SIZEL structure is identical to a <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -param iFormatCompat

Specifies the compatible engine format of the device surface being created. This is used by GDI if a temporary buffer is needed to simulate a complicated drawing call.

## -returns

The return value is a handle that identifies the surface if the function is successful. Otherwise, it is zero, and an error code is logged.

## -remarks

The storage space for the surface can optionally be provided by the driver. The surface should be associated by using <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>. The surface should be deleted when it is no longer needed by using <a href="/windows/desktop/api/winddi/nf-winddi-engdeletesurface">EngDeleteSurface</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletesurface">EngDeleteSurface</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>