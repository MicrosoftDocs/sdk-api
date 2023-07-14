---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetTag
title: IDvbFrequencyListDescriptor::GetTag (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbFrequencyListDescriptor interface","IDvbFrequencyListDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbFrequencyListDescriptor.GetTag","IDvbFrequencyListDescriptor::GetTag","IDvbFrequencyListDescriptorGetTag","dvbsiparser/IDvbFrequencyListDescriptor::GetTag","mstv.idvbfrequencylistdescriptor_gettag"]
old-location: mstv\idvbfrequencylistdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 05c607b4-c5de-4a57-93c0-412c85d9f2fa
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbFrequencyListDescriptor.GetTag, IDvbFrequencyListDescriptor::GetTag, IDvbFrequencyListDescriptorGetTag, dvbsiparser/IDvbFrequencyListDescriptor::GetTag, mstv.idvbfrequencylistdescriptor_gettag
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
 - IDvbFrequencyListDescriptor::GetTag
 - dvbsiparser/IDvbFrequencyListDescriptor::GetTag
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
 - IDvbFrequencyListDescriptor.GetTag
---

# IDvbFrequencyListDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTag</b> method returns the descriptor tag.

## -parameters

### -param pbVal [out]

Receives the descriptor tag.

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