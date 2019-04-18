---
UID: NF:d2d1svg.ID2D1SvgStrokeDashArray.GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32)
title: ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32) (d2d1svg.h)
author: windows-sdk-content
description: Gets dashes from the array.
old-location: direct2d\id2d1svgstrokedasharray_getdashes_2.htm
tech.root: Direct2D
ms.assetid: D439F7ED-608B-4A3B-891E-02A9ABD7C537
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDashes, GetDashes method [Direct2D], GetDashes method [Direct2D],ID2D1SvgStrokeDashArray interface, ID2D1SvgStrokeDashArray interface [Direct2D],GetDashes method, ID2D1SvgStrokeDashArray.GetDashes, ID2D1SvgStrokeDashArray.GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32), ID2D1SvgStrokeDashArray::GetDashes, ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32), d2d1svg/ID2D1SvgStrokeDashArray::GetDashes, direct2d.id2d1svgstrokedasharray_getdashes_2
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
 - ID2D1SvgStrokeDashArray.GetDashes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32)


## -description


Gets dashes from the array.


## -parameters




### -param dashes [out]

Type: <b><a href="https://msdn.microsoft.com/6DD79037-0BF2-4C1B-A2E3-85EB77682FB6">D2D1_SVG_LENGTH</a>*</b>

Buffer to contain the dashes.


### -param dashesCount

Type: <b>UINT32</b>

The element count of the array in the dashes argument.


### -param startIndex

Type: <b>UINT32</b>

The index of the first dash to retrieve.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/D3C82EC8-4172-48FE-AE8C-5F15BDBBCD30">ID2D1SvgStrokeDashArray</a>
 

 

