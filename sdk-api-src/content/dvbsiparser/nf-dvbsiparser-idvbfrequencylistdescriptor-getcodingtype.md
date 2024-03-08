---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetCodingType
title: IDvbFrequencyListDescriptor::GetCodingType (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCodingType","GetCodingType method [Microsoft TV Technologies]","GetCodingType method [Microsoft TV Technologies]","IDvbFrequencyListDescriptor interface","IDvbFrequencyListDescriptor interface [Microsoft TV Technologies]","GetCodingType method","IDvbFrequencyListDescriptor.GetCodingType","IDvbFrequencyListDescriptor::GetCodingType","IDvbFrequencyListDescriptorGetCodingType","dvbsiparser/IDvbFrequencyListDescriptor::GetCodingType","mstv.idvbfrequencylistdescriptor_getcodingtype"]
old-location: mstv\idvbfrequencylistdescriptor_getcodingtype.htm
tech.root: mstv
ms.assetid: 0d458f42-bea5-4503-a2d7-89efd1abc1a8
ms.date: 12/05/2018
ms.keywords: GetCodingType, GetCodingType method [Microsoft TV Technologies], GetCodingType method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetCodingType method, IDvbFrequencyListDescriptor.GetCodingType, IDvbFrequencyListDescriptor::GetCodingType, IDvbFrequencyListDescriptorGetCodingType, dvbsiparser/IDvbFrequencyListDescriptor::GetCodingType, mstv.idvbfrequencylistdescriptor_getcodingtype
req.header: dvbsiparser.h
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
 - IDvbFrequencyListDescriptor::GetCodingType
 - dvbsiparser/IDvbFrequencyListDescriptor::GetCodingType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbFrequencyListDescriptor.GetCodingType
---

# IDvbFrequencyListDescriptor::GetCodingType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCodingType</b> method returns a flag that specifies how the frequency is coded.

## -parameters

### -param pbVal [out]

Receives the coding_type flag.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbfrequencylistdescriptor">IDvbFrequencyListDescriptor Interface</a>