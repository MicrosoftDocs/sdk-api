---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRecordRatingDimension
title: IAtscContentAdvisoryDescriptor::GetRecordRatingDimension
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsccontentadvisorydescriptor_getrecordratingdimension.htm
old-project: mstv
ms.assetid: 583c9d8b-6b4b-4aa0-995d-26295b430f76
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordRatingDimension, GetRecordRatingDimension method [Microsoft TV Technologies], GetRecordRatingDimension method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRecordRatingDimension method, IAtscContentAdvisoryDescriptor.GetRecordRatingDimension, IAtscContentAdvisoryDescriptor::GetRecordRatingDimension, IAtscContentAdvisoryDescriptorGetRecordRatingDimension, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingDimension, mstv.iatsccontentadvisorydescriptor_getrecordratingdimension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: atscpsipparser.h
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor.GetRecordRatingDimension
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAtscContentAdvisoryDescriptor::GetRecordRatingDimension


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRatingDimension</b> method returns the dimension index into the rating region table (RRT) for a specified region.


## -parameters




### -param bIndexOuter [in]

Zero-based index of the rating region. To get the number of rating regions, call <a href="https://msdn.microsoft.com/e9571bdb-5b0b-4798-b4dc-37ccee51a8b3">IAtscContentAdvisoryDescriptor::GetRatingRegionCount</a>.


### -param bIndexInner [in]

Zero-based index of the rating dimension. To get the number of rating dimensions, call <a href="https://msdn.microsoft.com/6f0a8073-0361-4320-a5d9-7c536a07e9c3">IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions</a>.


### -param pbVal [out]

Receives the rating_dimension_j field.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>bIndexOuter</i> or <i>bIndexInner</i> parameter is out of bounds.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b7379d66-c57b-45e0-9c63-901bf3637f21">IAtscContentAdvisoryDescriptor Interface</a>
 

 

