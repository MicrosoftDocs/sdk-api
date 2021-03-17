---
UID: NF:winddi.DrvDescribePixelFormat
title: DrvDescribePixelFormat function (winddi.h)
description: The DrvDescribePixelFormat function describes the pixel format for a device-specified PDEV by writing a pixel format description to a PIXELFORMATDESCRIPTOR structure.
helpviewer_keywords: ["DrvDescribePixelFormat","DrvDescribePixelFormat function [Display Devices]","ddifncs_ad08e90b-a4e1-43e3-bbd7-8476d1c5568b.xml","display.drvdescribepixelformat","winddi/DrvDescribePixelFormat"]
old-location: display\drvdescribepixelformat.htm
tech.root: display
ms.assetid: 7c630694-e076-4ab2-a2c9-262c7c5da988
ms.date: 12/05/2018
ms.keywords: DrvDescribePixelFormat, DrvDescribePixelFormat function [Display Devices], ddifncs_ad08e90b-a4e1-43e3-bbd7-8476d1c5568b.xml, display.drvdescribepixelformat, winddi/DrvDescribePixelFormat
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
 - DrvDescribePixelFormat
 - winddi/DrvDescribePixelFormat
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
 - DrvDescribePixelFormat
---

# DrvDescribePixelFormat function


## -description

The <b>DrvDescribePixelFormat</b> function describes the pixel format for a device-specified <a href="/windows-hardware/drivers/">PDEV</a> by writing a pixel format description to a PIXELFORMATDESCRIPTOR structure.

## -parameters

### -param dhpdev

Identifies the device for which pixel format information is requested.

### -param iPixelFormat

Specifies the index number of the requested pixel format.

### -param cjpfd

Specifies the maximum number of bytes that can be written to the structure pointed to by <i>ppfd</i>.

### -param ppfd

Pointer to a PIXELFORMATDESCRIPTOR structure (described in the Microsoft Windows SDK documentation) that is to receive information about the pixel format. This parameter can be <b>NULL</b>.

## -returns

The return value is the maximum pixel format index if the function is successful. Otherwise, it is zero, and an error code is logged.

## -remarks

A display driver that supports 3D graphics hardware can support windows with different pixel formats on a single display surface. The pixel format must correspond to a configuration supported by the graphics hardware.

<b>DrvDescribePixelFormat</b> fills in the structure pointed to by <i>ppfd</i> if this parameter is not <b>NULL</b>.

The returned maximum pixel format index can be used by applications that need to obtain a device context's maximum pixel format index. The pixel formats that a device supports are identified by positive one-based integer indices.

The pixel format functions are used in conjunction with the window object services functions to track and update pixel formats of windows on a display surface.