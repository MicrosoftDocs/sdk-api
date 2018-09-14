---
UID: NF:d2d1svg.ID2D1SvgDocument.CreatePointCollection
title: ID2D1SvgDocument::CreatePointCollection
author: windows-sdk-content
description: Creates a points object which can be used to set a points attribute on a polygon or polyline element.
old-location: direct2d\id2d1svgdocument_createpointcollection.htm
tech.root: Direct2D
ms.assetid: A7AB02F2-32B0-4FF5-8A3A-CE7A6AD9DB57
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreatePointCollection, CreatePointCollection method [Direct2D], CreatePointCollection method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreatePointCollection method, ID2D1SvgDocument.CreatePointCollection, ID2D1SvgDocument::CreatePointCollection, d2d1svg/ID2D1SvgDocument::CreatePointCollection, direct2d.id2d1svgdocument_createpointcollection
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
 - ID2D1SvgDocument.CreatePointCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument::CreatePointCollection


## -description


Creates a points object which can be used to set a points attribute on a polygon or polyline element.


## -parameters




### -param points [in, optional]

Type: <b>const D2D1_POINT_2F*</b>

The points in the point collection.


### -param pointsCount

Type: <b>UINT32</b>

The number of points in the points argument.


### -param pointCollection [out]

Type: <b>ID2D1SvgPointCollection**</b>

The created <a href="https://msdn.microsoft.com/6033F923-35E1-400F-965F-2FBED95B260A">ID2D1SvgPointCollection</a> object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/1F570A77-7110-4C71-A7BE-74F2B78CFE96">ID2D1SvgDocument</a>
 

 

