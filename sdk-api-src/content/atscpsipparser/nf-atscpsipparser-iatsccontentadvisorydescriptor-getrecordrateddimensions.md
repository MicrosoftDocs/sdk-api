---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRecordRatedDimensions
title: IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsccontentadvisorydescriptor_getrecordrateddimensions.htm
tech.root: mstv
ms.assetid: 6f0a8073-0361-4320-a5d9-7c536a07e9c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordRatedDimensions, GetRecordRatedDimensions method [Microsoft TV Technologies], GetRecordRatedDimensions method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRecordRatedDimensions method, IAtscContentAdvisoryDescriptor.GetRecordRatedDimensions, IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions, IAtscContentAdvisoryDescriptorGetRecordRatedDimensions, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions, mstv.iatsccontentadvisorydescriptor_getrecordrateddimensions
ms.topic: method
f1_keywords: 
 - "atscpsipparser/IAtscContentAdvisoryDescriptor.GetRecordRatedDimensions"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor.GetRecordRatedDimensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRatedDimensions</b> method returns the number of rating dimensions for a specified rating region.


## -parameters




### -param bIndex [in]

Zero-based index of the rating region. To get the number of rating regions, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsccontentadvisorydescriptor-getratingregioncount">IAtscContentAdvisoryDescriptor::GetRatingRegionCount</a>.


### -param pbVal [out]

Receives the rated_dimensions field.


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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>bIndex</i> parameter is out of bounds.

</td>
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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsccontentadvisorydescriptor">IAtscContentAdvisoryDescriptor Interface</a>
 

 

