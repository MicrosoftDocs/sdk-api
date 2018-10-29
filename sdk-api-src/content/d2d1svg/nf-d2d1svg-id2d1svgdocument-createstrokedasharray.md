---
UID: NF:d2d1svg.ID2D1SvgDocument.CreateStrokeDashArray
title: ID2D1SvgDocument::CreateStrokeDashArray
author: windows-sdk-content
description: Creates a dash array object which can be used to set the stroke-dasharray property.
old-location: direct2d\id2d1svgdocument_createstrokedasharray.htm
tech.root: Direct2D
ms.assetid: 559330E4-A0B9-437A-AD83-02C9409B5BE2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateStrokeDashArray, CreateStrokeDashArray method [Direct2D], CreateStrokeDashArray method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreateStrokeDashArray method, ID2D1SvgDocument.CreateStrokeDashArray, ID2D1SvgDocument::CreateStrokeDashArray, d2d1svg/ID2D1SvgDocument::CreateStrokeDashArray, direct2d.id2d1svgdocument_createstrokedasharray
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
 - ID2D1SvgDocument.CreateStrokeDashArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument::CreateStrokeDashArray


## -description


Creates a dash array object which can be used to set the stroke-dasharray property.


## -parameters




### -param dashes [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/6DD79037-0BF2-4C1B-A2E3-85EB77682FB6">D2D1_SVG_LENGTH</a>*</b>

An array of dashes.


### -param dashesCount

Type: <b>UINT32</b>

Size of the array in th dashes argument.


### -param strokeDashArray [out]

Type: <b>ID2D1SvgStrokeDashArray**</b>

The created <a href="https://msdn.microsoft.com/D3C82EC8-4172-48FE-AE8C-5F15BDBBCD30">ID2D1SvgStrokeDashArray</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/1F570A77-7110-4C71-A7BE-74F2B78CFE96">ID2D1SvgDocument</a>
 

 

