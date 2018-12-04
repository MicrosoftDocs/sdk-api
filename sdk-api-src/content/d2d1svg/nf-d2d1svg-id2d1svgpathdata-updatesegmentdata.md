---
UID: NF:d2d1svg.ID2D1SvgPathData.UpdateSegmentData
title: ID2D1SvgPathData::UpdateSegmentData
author: windows-sdk-content
description: Updates the segment data array. Existing segment data not updated by this method are preserved. The array is resized larger if necessary to accomodate the new segment data.
old-location: direct2d\id2d1svgpathdata_updatesegmentdata.htm
tech.root: direct2d
ms.assetid: 3B87B002-7F1C-4531-B584-C0CFC8E46256
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID2D1SvgPathData interface [Direct2D],UpdateSegmentData method, ID2D1SvgPathData.UpdateSegmentData, ID2D1SvgPathData::UpdateSegmentData, UpdateSegmentData, UpdateSegmentData method [Direct2D], UpdateSegmentData method [Direct2D],ID2D1SvgPathData interface, d2d1svg/ID2D1SvgPathData::UpdateSegmentData, direct2d.id2d1svgpathdata_updatesegmentdata
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
 - ID2D1SvgPathData.UpdateSegmentData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPathData::UpdateSegmentData


## -description


Updates the segment data array. Existing segment data not updated by this method are preserved. 
        The array is resized larger if necessary to accomodate the new segment data.


## -parameters




### -param data [in]

Type: <b>const FLOAT*</b>

The data array.


### -param dataCount

Type: <b>UINT32</b>

The number of data to update.


### -param startIndex

Type: <b>UINT32</b>

The index at which to begin updating segment data. Must be less than or equal to the size of the segment data array.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/14879B17-0CAA-42E7-8643-7D385EABFD37">ID2D1SvgPathData</a>
 

 

