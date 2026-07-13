---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetCCType
title: ICaptionServiceDescriptor::GetCCType (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCCType","GetCCType method [Microsoft TV Technologies]","GetCCType method [Microsoft TV Technologies]","ICaptionServiceDescriptor interface","ICaptionServiceDescriptor interface [Microsoft TV Technologies]","GetCCType method","ICaptionServiceDescriptor.GetCCType","ICaptionServiceDescriptor::GetCCType","ICaptionServiceDescriptorGetCCType","atscpsipparser/ICaptionServiceDescriptor::GetCCType","mstv.icaptionservicedescriptor_getcctype"]
old-location: mstv\icaptionservicedescriptor_getcctype.htm
tech.root: mstv
ms.assetid: d245118a-3ff2-4ea7-9ff9-f8c1991f2073
ms.date: 12/05/2018
ms.keywords: GetCCType, GetCCType method [Microsoft TV Technologies], GetCCType method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetCCType method, ICaptionServiceDescriptor.GetCCType, ICaptionServiceDescriptor::GetCCType, ICaptionServiceDescriptorGetCCType, atscpsipparser/ICaptionServiceDescriptor::GetCCType, mstv.icaptionservicedescriptor_getcctype
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
 - ICaptionServiceDescriptor::GetCCType
 - atscpsipparser/ICaptionServiceDescriptor::GetCCType
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
 - ICaptionServiceDescriptor.GetCCType
---

# ICaptionServiceDescriptor::GetCCType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCCType</b> method queries whether a caption service contains Digital Television Closed Captioning (DTVCC) or line-21 closed captioning.

## -parameters

### -param bIndex [in]

Zero-based index of the caption service. To get the number of caption services, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-icaptionservicedescriptor-getnumberofservices">ICaptionServiceDescriptor::GetNumberOfServices</a>.

### -param pbVal [out]

Receives the cc_type flag:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The caption service contains line-21 captions.</td>
</tr>
<tr>
<td>1</td>
<td>The caption service contains DTVCC captions.</td>
</tr>
</table>

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
<dt><b>MPEG2_E_INCORRECT_DESCRIPTOR_TAG</b></dt>
</dl>
</td>
<td width="60%">
The table descriptor tag is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The PSIP table is not well formed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>bIndex</i> parameter is out of range.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-icaptionservicedescriptor">ICaptionServiceDescriptor Interface</a>