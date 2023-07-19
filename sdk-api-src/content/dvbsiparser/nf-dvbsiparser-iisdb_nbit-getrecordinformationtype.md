---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordInformationType
title: IISDB_NBIT::GetRecordInformationType (dvbsiparser.h)
description: Gets an information_type field from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetRecordInformationType","GetRecordInformationType method [Microsoft TV Technologies]","GetRecordInformationType method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordInformationType method","IISDB_NBIT.GetRecordInformationType","IISDB_NBIT::GetRecordInformationType","dvbsiparser/IISDB_NBIT::GetRecordInformationType","mstv.iisdb_nbit_getrecordinformationtype"]
old-location: mstv\iisdb_nbit_getrecordinformationtype.htm
tech.root: mstv
ms.assetid: 0f51abc1-d797-4666-b5d5-50560fd2f9f3
ms.date: 12/05/2018
ms.keywords: GetRecordInformationType, GetRecordInformationType method [Microsoft TV Technologies], GetRecordInformationType method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordInformationType method, IISDB_NBIT.GetRecordInformationType, IISDB_NBIT::GetRecordInformationType, dvbsiparser/IISDB_NBIT::GetRecordInformationType, mstv.iisdb_nbit_getrecordinformationtype
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
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
 - IISDB_NBIT::GetRecordInformationType
 - dvbsiparser/IISDB_NBIT::GetRecordInformationType
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
 - IISDB_NBIT.GetRecordInformationType
---

# IISDB_NBIT::GetRecordInformationType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an information_type field from 
  a record in an Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a> method to get the number of records in the NBIT.

### -param pbVal [out]

Receives the information_type field. This field can contain any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Undefined

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Information (key ID: none)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Information with service identifier (key ID: service identifier)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
Information with genre (key ID: content_nibble, user_nibble)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x4 - 0xF</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a>