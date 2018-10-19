---
UID: NF:d2d1svg.ID2D1SvgDocument.CreatePathData
title: ID2D1SvgDocument::CreatePathData
author: windows-sdk-content
description: Creates a path data object which can be used to set a 'd' attribute on a 'path' element.
old-location: direct2d\id2d1svgdocument_createpathdata.htm
tech.root: direct2d
ms.assetid: 3BF28252-AC33-4B16-9A72-2838006C4A21
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CreatePathData, CreatePathData method [Direct2D], CreatePathData method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreatePathData method, ID2D1SvgDocument.CreatePathData, ID2D1SvgDocument::CreatePathData, d2d1svg/ID2D1SvgDocument::CreatePathData, direct2d.id2d1svgdocument_createpathdata
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
 - ID2D1SvgDocument.CreatePathData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument::CreatePathData


## -description


Creates a path data object which can be used to set a 'd' attribute on a 'path' element.


## -parameters




### -param segmentData [in, optional]

Type: <b>const FLOAT*</b>

An array of segment data.


### -param segmentDataCount

Type: <b>UINT32</b>

Number of items in segmentData.


### -param commands [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/E0A5F435-F4FB-4CD3-84B3-962CB7B96446">D2D1_SVG_PATH_COMMAND</a>*</b>

An array of path commands.


### -param commandsCount

Type: <b>UINT32</b>

The number of items in commands.


### -param pathData [out]

Type: <b>ID2D1SvgPathData**</b>

When this method completes, this points to the created path data.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/1F570A77-7110-4C71-A7BE-74F2B78CFE96">ID2D1SvgDocument</a>
 

 

