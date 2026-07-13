---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRecordRatingDimension
title: IAtscContentAdvisoryDescriptor::GetRecordRatingDimension (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordRatingDimension","GetRecordRatingDimension method [Microsoft TV Technologies]","GetRecordRatingDimension method [Microsoft TV Technologies]","IAtscContentAdvisoryDescriptor interface","IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies]","GetRecordRatingDimension method","IAtscContentAdvisoryDescriptor.GetRecordRatingDimension","IAtscContentAdvisoryDescriptor::GetRecordRatingDimension","IAtscContentAdvisoryDescriptorGetRecordRatingDimension","atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingDimension","mstv.iatsccontentadvisorydescriptor_getrecordratingdimension"]
old-location: mstv\iatsccontentadvisorydescriptor_getrecordratingdimension.htm
tech.root: mstv
ms.assetid: 583c9d8b-6b4b-4aa0-995d-26295b430f76
ms.date: 12/05/2018
ms.keywords: GetRecordRatingDimension, GetRecordRatingDimension method [Microsoft TV Technologies], GetRecordRatingDimension method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRecordRatingDimension method, IAtscContentAdvisoryDescriptor.GetRecordRatingDimension, IAtscContentAdvisoryDescriptor::GetRecordRatingDimension, IAtscContentAdvisoryDescriptorGetRecordRatingDimension, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingDimension, mstv.iatsccontentadvisorydescriptor_getrecordratingdimension
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAtscContentAdvisoryDescriptor::GetRecordRatingDimension
 - atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingDimension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor.GetRecordRatingDimension
---

# IAtscContentAdvisoryDescriptor::GetRecordRatingDimension


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRatingDimension</b> method returns the dimension index into the rating region table (RRT) for a specified region.

## -parameters

### -param bIndexOuter [in]

Zero-based index of the rating region. To get the number of rating regions, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsccontentadvisorydescriptor-getratingregioncount">IAtscContentAdvisoryDescriptor::GetRatingRegionCount</a>.

### -param bIndexInner [in]

Zero-based index of the rating dimension. To get the number of rating dimensions, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsccontentadvisorydescriptor-getrecordrateddimensions">IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions</a>.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsccontentadvisorydescriptor">IAtscContentAdvisoryDescriptor Interface</a>