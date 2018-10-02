---
UID: NF:d2d1svg.ID2D1SvgDocument.FindElementById
title: ID2D1SvgDocument::FindElementById
author: windows-sdk-content
description: Gets the SVG element with the specified ID.
old-location: direct2d\id2d1svgdocument_findelementbyid.htm
tech.root: direct2d
ms.assetid: B4E4EE0E-0A2B-479A-B101-AC9DF8546A4F
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: FindElementById, FindElementById method [Direct2D], FindElementById method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],FindElementById method, ID2D1SvgDocument.FindElementById, ID2D1SvgDocument::FindElementById, d2d1svg/ID2D1SvgDocument::FindElementById, direct2d.id2d1svgdocument_findelementbyid
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
 - ID2D1SvgDocument.FindElementById
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument::FindElementById


## -description


Gets the SVG element with the specified ID. 


## -parameters




### -param id [in]

Type: <b>PCWSTR</b>

ID of the element to retrieve.


### -param svgElement

Type: <b>ID2D1SvgElement**</b>

The element matching the specified ID. If the element cannot be found, the returned element will be null.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/1F570A77-7110-4C71-A7BE-74F2B78CFE96">ID2D1SvgDocument</a>
 

 

