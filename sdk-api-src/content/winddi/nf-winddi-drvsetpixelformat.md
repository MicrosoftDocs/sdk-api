---
UID: NF:winddi.DrvSetPixelFormat
title: DrvSetPixelFormat function (winddi.h)
description: The DrvSetPixelFormat function sets the pixel format of a window.
helpviewer_keywords: ["DrvSetPixelFormat","DrvSetPixelFormat function [Display Devices]","ddifncs_095cf66c-832a-49c2-9bf2-f97ef74665b2.xml","display.drvsetpixelformat","winddi/DrvSetPixelFormat"]
old-location: display\drvsetpixelformat.htm
tech.root: display
ms.assetid: b2211639-13ae-455c-97ef-8145318af591
ms.date: 12/05/2018
ms.keywords: DrvSetPixelFormat, DrvSetPixelFormat function [Display Devices], ddifncs_095cf66c-832a-49c2-9bf2-f97ef74665b2.xml, display.drvsetpixelformat, winddi/DrvSetPixelFormat
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvSetPixelFormat
 - winddi/DrvSetPixelFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSetPixelFormat
---

# DrvSetPixelFormat function


## -description

The <b>DrvSetPixelFormat</b> function sets the pixel format of a window.

## -parameters

### -param pso

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure with which the window is associated.

### -param iPixelFormat

Index that specifies the device format to which the pixel format is to be set. The pixel formats that a device supports are identified by positive one-based integer indices starting at 1.

### -param hwnd

Handle to the window whose pixel format is to be set.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

Setting the pixel format more than once can result in complications for Window Manager and for multithreaded applications. Consequently, the pixel format of a window can be set only once and must remain unchanged.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvdescribepixelformat">DrvDescribePixelFormat</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>