---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRatingRegionCount
title: IAtscContentAdvisoryDescriptor::GetRatingRegionCount (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRatingRegionCount","GetRatingRegionCount method [Microsoft TV Technologies]","GetRatingRegionCount method [Microsoft TV Technologies]","IAtscContentAdvisoryDescriptor interface","IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies]","GetRatingRegionCount method","IAtscContentAdvisoryDescriptor.GetRatingRegionCount","IAtscContentAdvisoryDescriptor::GetRatingRegionCount","IAtscContentAdvisoryDescriptorGetRatingRegionCount","atscpsipparser/IAtscContentAdvisoryDescriptor::GetRatingRegionCount","mstv.iatsccontentadvisorydescriptor_getratingregioncount"]
old-location: mstv\iatsccontentadvisorydescriptor_getratingregioncount.htm
tech.root: mstv
ms.assetid: e9571bdb-5b0b-4798-b4dc-37ccee51a8b3
ms.date: 12/05/2018
ms.keywords: GetRatingRegionCount, GetRatingRegionCount method [Microsoft TV Technologies], GetRatingRegionCount method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRatingRegionCount method, IAtscContentAdvisoryDescriptor.GetRatingRegionCount, IAtscContentAdvisoryDescriptor::GetRatingRegionCount, IAtscContentAdvisoryDescriptorGetRatingRegionCount, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRatingRegionCount, mstv.iatsccontentadvisorydescriptor_getratingregioncount
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
 - IAtscContentAdvisoryDescriptor::GetRatingRegionCount
 - atscpsipparser/IAtscContentAdvisoryDescriptor::GetRatingRegionCount
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
 - IAtscContentAdvisoryDescriptor.GetRatingRegionCount
---

# IAtscContentAdvisoryDescriptor::GetRatingRegionCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRatingRegionCount</b> method returns the number of rating regions.

## -parameters

### -param pbVal [out]

Receives the rating_region_count field.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsccontentadvisorydescriptor">IAtscContentAdvisoryDescriptor Interface</a>