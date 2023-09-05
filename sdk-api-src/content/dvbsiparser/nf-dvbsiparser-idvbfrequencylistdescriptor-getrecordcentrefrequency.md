---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetRecordCentreFrequency
title: IDvbFrequencyListDescriptor::GetRecordCentreFrequency (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordCentreFrequency","GetRecordCentreFrequency method [Microsoft TV Technologies]","GetRecordCentreFrequency method [Microsoft TV Technologies]","IDvbFrequencyListDescriptor interface","IDvbFrequencyListDescriptor interface [Microsoft TV Technologies]","GetRecordCentreFrequency method","IDvbFrequencyListDescriptor.GetRecordCentreFrequency","IDvbFrequencyListDescriptor::GetRecordCentreFrequency","IDvbFrequencyListDescriptorGetRecordCentreFrequency","dvbsiparser/IDvbFrequencyListDescriptor::GetRecordCentreFrequency","mstv.idvbfrequencylistdescriptor_getrecordcentrefrequency"]
old-location: mstv\idvbfrequencylistdescriptor_getrecordcentrefrequency.htm
tech.root: mstv
ms.assetid: bb6c3c14-c4b6-412d-ad12-1c7fdb025527
ms.date: 12/05/2018
ms.keywords: GetRecordCentreFrequency, GetRecordCentreFrequency method [Microsoft TV Technologies], GetRecordCentreFrequency method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetRecordCentreFrequency method, IDvbFrequencyListDescriptor.GetRecordCentreFrequency, IDvbFrequencyListDescriptor::GetRecordCentreFrequency, IDvbFrequencyListDescriptorGetRecordCentreFrequency, dvbsiparser/IDvbFrequencyListDescriptor::GetRecordCentreFrequency, mstv.idvbfrequencylistdescriptor_getrecordcentrefrequency
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
 - IDvbFrequencyListDescriptor::GetRecordCentreFrequency
 - dvbsiparser/IDvbFrequencyListDescriptor::GetRecordCentreFrequency
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
 - IDvbFrequencyListDescriptor.GetRecordCentreFrequency
---

# IDvbFrequencyListDescriptor::GetRecordCentreFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCentreFrequency</b> method returns the frequency at a specified index in the frequency list.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the frequency to return. To get the number of frequencies in the descriptor, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbfrequencylistdescriptor-getcountofrecords">IDvbFrequencyListDescriptor::GetCountOfRecords</a>.

### -param pdwVal [out]

Receives the centre_frequency field.

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