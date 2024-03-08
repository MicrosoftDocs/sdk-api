---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetCountOfRecords
title: IDvbFrequencyListDescriptor::GetCountOfRecords (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbFrequencyListDescriptor interface","IDvbFrequencyListDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbFrequencyListDescriptor.GetCountOfRecords","IDvbFrequencyListDescriptor::GetCountOfRecords","IDvbFrequencyListDescriptorGetCountOfRecords","dvbsiparser/IDvbFrequencyListDescriptor::GetCountOfRecords","mstv.idvbfrequencylistdescriptor_getcountofrecords"]
old-location: mstv\idvbfrequencylistdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 9bce2abf-2673-49c6-8b87-7c8825544156
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbFrequencyListDescriptor.GetCountOfRecords, IDvbFrequencyListDescriptor::GetCountOfRecords, IDvbFrequencyListDescriptorGetCountOfRecords, dvbsiparser/IDvbFrequencyListDescriptor::GetCountOfRecords, mstv.idvbfrequencylistdescriptor_getcountofrecords
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbFrequencyListDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbFrequencyListDescriptor::GetCountOfRecords
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
 - IDvbFrequencyListDescriptor.GetCountOfRecords
---

# IDvbFrequencyListDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the frequency list descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

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