---
UID: NF:d2d1svg.ID2D1SvgPathData.GetSegmentData
title: ID2D1SvgPathData::GetSegmentData
author: windows-sdk-content
description: Gets data from the segment data array.
old-location: direct2d\id2d1svgpathdata_getsegmentdata.htm
tech.root: direct2d
ms.assetid: D935BCEB-D7B8-4245-AD1C-25BAE63F8944
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetSegmentData, GetSegmentData method [Direct2D], GetSegmentData method [Direct2D],ID2D1SvgPathData interface, ID2D1SvgPathData interface [Direct2D],GetSegmentData method, ID2D1SvgPathData.GetSegmentData, ID2D1SvgPathData::GetSegmentData, d2d1svg/ID2D1SvgPathData::GetSegmentData, direct2d.id2d1svgpathdata_getsegmentdata
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
 - ID2D1SvgPathData.GetSegmentData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPathData::GetSegmentData


## -description


Gets data from the segment data array.


## -parameters




### -param data [out]

Type: <b>FLOAT*</b>

Buffer to contain the segment data array.


### -param dataCount

Type: <b>UINT32</b>

The element count of the buffer.


### -param startIndex

Type: <b>UINT32</b>

The index of the first segment data to retrieve.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/14879B17-0CAA-42E7-8643-7D385EABFD37">ID2D1SvgPathData</a>
 

 

