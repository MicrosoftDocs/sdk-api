---
UID: NF:d2d1svg.ID2D1SvgStrokeDashArray.UpdateDashes(const FLOAT,UINT32,UINT32)
title: ID2D1SvgStrokeDashArray::UpdateDashes(const FLOAT,UINT32,UINT32) (d2d1svg.h)
author: windows-sdk-content
description: Updates the array. Existing dashes not updated by this method are preserved. The array is resized larger if necessary to accomodate the new dashes.
old-location: direct2d\id2d1svgstrokedasharray_updatedashes.htm
tech.root: Direct2D
ms.assetid: 8F33A62C-C503-4CAE-8887-A00CE368BD6F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgStrokeDashArray interface [Direct2D],UpdateDashes method, ID2D1SvgStrokeDashArray.UpdateDashes, ID2D1SvgStrokeDashArray.UpdateDashes(const FLOAT,UINT32,UINT32), ID2D1SvgStrokeDashArray::UpdateDashes, ID2D1SvgStrokeDashArray::UpdateDashes(const FLOAT,UINT32,UINT32), UpdateDashes, UpdateDashes method [Direct2D], UpdateDashes method [Direct2D],ID2D1SvgStrokeDashArray interface, d2d1svg/ID2D1SvgStrokeDashArray::UpdateDashes, direct2d.id2d1svgstrokedasharray_updatedashes
ms.topic: method
f1_keywords: 
 - "d2d1svg/ID2D1SvgStrokeDashArray.UpdateDashes"
dev_langs:
 - c++
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
 - ID2D1SvgStrokeDashArray.UpdateDashes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgStrokeDashArray::UpdateDashes(const FLOAT,UINT32,UINT32)


## -description


Updates the array. Existing dashes not updated by this method are preserved. The array is resized larger if necessary to accomodate the new dashes.


## -parameters




### -param dashes [in]

Type: <b>const FLOAT*</b>

The dashes array.


### -param dashesCount

Type: <b>UINT32</b>

The number of dashes to update.


### -param startIndex

Type: <b>UINT32</b>

The index at which to begin updating dashes. Must be less than or equal to the size of the array.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgstrokedasharray">ID2D1SvgStrokeDashArray</a>
 

 

