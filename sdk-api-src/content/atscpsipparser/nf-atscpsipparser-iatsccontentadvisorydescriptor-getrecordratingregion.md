---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRecordRatingRegion
title: IAtscContentAdvisoryDescriptor::GetRecordRatingRegion (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordRatingRegion","GetRecordRatingRegion method [Microsoft TV Technologies]","GetRecordRatingRegion method [Microsoft TV Technologies]","IAtscContentAdvisoryDescriptor interface","IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies]","GetRecordRatingRegion method","IAtscContentAdvisoryDescriptor.GetRecordRatingRegion","IAtscContentAdvisoryDescriptor::GetRecordRatingRegion","IAtscContentAdvisoryDescriptorGetRecordRatingRegion","atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingRegion","mstv.iatsccontentadvisorydescriptor_getrecordratingregion"]
old-location: mstv\iatsccontentadvisorydescriptor_getrecordratingregion.htm
tech.root: mstv
ms.assetid: fb828399-d4aa-4e35-bb77-16795a598b35
ms.date: 12/05/2018
ms.keywords: GetRecordRatingRegion, GetRecordRatingRegion method [Microsoft TV Technologies], GetRecordRatingRegion method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRecordRatingRegion method, IAtscContentAdvisoryDescriptor.GetRecordRatingRegion, IAtscContentAdvisoryDescriptor::GetRecordRatingRegion, IAtscContentAdvisoryDescriptorGetRecordRatingRegion, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingRegion, mstv.iatsccontentadvisorydescriptor_getrecordratingregion
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
 - IAtscContentAdvisoryDescriptor::GetRecordRatingRegion
 - atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingRegion
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
 - IAtscContentAdvisoryDescriptor.GetRecordRatingRegion
---

# IAtscContentAdvisoryDescriptor::GetRecordRatingRegion


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRatingRegion</b> method returns the rating region at a specified index.

## -parameters

### -param bIndex [in]

Zero-based index of the rating region. To get the number of rating regions, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsccontentadvisorydescriptor-getratingregioncount">IAtscContentAdvisoryDescriptor::GetRatingRegionCount</a>.

### -param pbVal [out]

Receives the rating_region field.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsccontentadvisorydescriptor">IAtscContentAdvisoryDescriptor Interface</a>