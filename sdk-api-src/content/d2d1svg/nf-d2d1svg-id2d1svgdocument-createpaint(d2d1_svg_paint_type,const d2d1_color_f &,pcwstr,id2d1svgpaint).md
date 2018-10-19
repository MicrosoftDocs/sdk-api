---
UID: NF:d2d1svg.ID2D1SvgDocument.CreatePaint(D2D1_SVG_PAINT_TYPE,const D2D1_COLOR_F &,PCWSTR,ID2D1SvgPaint)
title: ID2D1SvgDocument::CreatePaint(D2D1_SVG_PAINT_TYPE,const D2D1_COLOR_F &,PCWSTR,ID2D1SvgPaint)
author: windows-sdk-content
description: Creates a paint object which can be used to set the 'fill' or 'stroke' properties.
old-location: direct2d\id2d1svgdocument_createpaint_2.htm
tech.root: direct2d
ms.assetid: 449b9df3-cb5c-015b-2ecc-c7617c1625c6
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CreatePaint, CreatePaint method [Direct2D], CreatePaint method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreatePaint method, ID2D1SvgDocument.CreatePaint, ID2D1SvgDocument.CreatePaint(D2D1_SVG_PAINT_TYPE,const D2D1_COLOR_F &,PCWSTR,ID2D1SvgPaint), ID2D1SvgDocument::CreatePaint, ID2D1SvgDocument::CreatePaint(D2D1_SVG_PAINT_TYPE,const D2D1_COLOR_F &,PCWSTR,ID2D1SvgPaint), d2d1svg/ID2D1SvgDocument::CreatePaint, direct2d.id2d1svgdocument_createpaint_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.dll: Direct2d.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgDocument.CreatePaint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument::CreatePaint(D2D1_SVG_PAINT_TYPE,const D2D1_COLOR_F &,PCWSTR,ID2D1SvgPaint)


## -description


Creates a paint object which can be used to set the 'fill' or 'stroke' properties.


## -parameters




### -param paintType

Type: <b><a href="https://msdn.microsoft.com/FBCD7EF5-E1DF-4FE0-98A2-40F42798FB93">D2D1_SVG_PAINT_TYPE</a></b>

Specifies the type of paint object to create.


### -param color [ref]

Type: <b>const D2D1_COLOR_F</b>

The color used if the paintType is D2D1_SVG_PAINT_TYPE_COLOR.


### -param id [in, optional]

Type: <b>PCWSTR</b>

The element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.


### -param paint [out]

Type: <b>ID2D1SvgPaint**</b>

When the method completes, this will contain a pointer to the created paint object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/1F570A77-7110-4C71-A7BE-74F2B78CFE96">ID2D1SvgDocument</a>
 

 

