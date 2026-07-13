---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRecordRatingValue
title: IAtscContentAdvisoryDescriptor::GetRecordRatingValue (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordRatingValue","GetRecordRatingValue method [Microsoft TV Technologies]","GetRecordRatingValue method [Microsoft TV Technologies]","IAtscContentAdvisoryDescriptor interface","IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies]","GetRecordRatingValue method","IAtscContentAdvisoryDescriptor.GetRecordRatingValue","IAtscContentAdvisoryDescriptor::GetRecordRatingValue","IAtscContentAdvisoryDescriptorGetRecordRatingValue","atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingValue","mstv.iatsccontentadvisorydescriptor_getrecordratingvalue"]
old-location: mstv\iatsccontentadvisorydescriptor_getrecordratingvalue.htm
tech.root: mstv
ms.assetid: c380d920-8d12-4965-8a5c-88e2f5861a09
ms.date: 12/05/2018
ms.keywords: GetRecordRatingValue, GetRecordRatingValue method [Microsoft TV Technologies], GetRecordRatingValue method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRecordRatingValue method, IAtscContentAdvisoryDescriptor.GetRecordRatingValue, IAtscContentAdvisoryDescriptor::GetRecordRatingValue, IAtscContentAdvisoryDescriptorGetRecordRatingValue, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingValue, mstv.iatsccontentadvisorydescriptor_getrecordratingvalue
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
 - IAtscContentAdvisoryDescriptor::GetRecordRatingValue
 - atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingValue
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
 - IAtscContentAdvisoryDescriptor.GetRecordRatingValue
---

# IAtscContentAdvisoryDescriptor::GetRecordRatingValue


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRatingValue</b> method returns the rating value of a specified rating dimension.

## -parameters

### -param bIndexOuter [in]

Zero-based index of the rating region. To get the number of rating regions, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsccontentadvisorydescriptor-getratingregioncount">IAtscContentAdvisoryDescriptor::GetRatingRegionCount</a>.

### -param bIndexInner [in]

Zero-based index of the rating dimension. To get the number of rating dimensions, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsccontentadvisorydescriptor-getrecordrateddimensions">IAtscContentAdvisoryDescriptor::GetRecordRatedDimensions</a>.

### -param pbVal [out]

Receives the rating_value field

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
The <i>bIndexOuter</i> or <i>bIndexInner</i> parameter is out of bounds.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsccontentadvisorydescriptor">IAtscContentAdvisoryDescriptor Interface</a>