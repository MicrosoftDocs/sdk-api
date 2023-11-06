---
UID: NF:dvbsiparser.IDvbSiParser2.GetEIT2
title: IDvbSiParser2::GetEIT2 (dvbsiparser.h)
description: .
helpviewer_keywords: ["DVB_EIT_ACTUAL_TID","DVB_EIT_OTHER_TID","GetEIT2","GetEIT2 method [Microsoft TV Technologies]","GetEIT2 method [Microsoft TV Technologies]","IDvbSiParser2 interface","IDvbSiParser2 interface [Microsoft TV Technologies]","GetEIT2 method","IDvbSiParser2.GetEIT2","IDvbSiParser2::GetEIT2","dvbsiparser/IDvbSiParser2::GetEIT2","mstv.idvbsiparser2_geteit2"]
old-location: mstv\idvbsiparser2_geteit2.htm
tech.root: mstv
ms.assetid: 47ccce59-d67e-4994-b69d-8dac425b375a
ms.date: 12/05/2018
ms.keywords: DVB_EIT_ACTUAL_TID, DVB_EIT_OTHER_TID, GetEIT2, GetEIT2 method [Microsoft TV Technologies], GetEIT2 method [Microsoft TV Technologies],IDvbSiParser2 interface, IDvbSiParser2 interface [Microsoft TV Technologies],GetEIT2 method, IDvbSiParser2.GetEIT2, IDvbSiParser2::GetEIT2, dvbsiparser/IDvbSiParser2::GetEIT2, mstv.idvbsiparser2_geteit2
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
 - IDvbSiParser2::GetEIT2
 - dvbsiparser/IDvbSiParser2::GetEIT2
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
 - IDvbSiParser2.GetEIT2
---

# IDvbSiParser2::GetEIT2


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetEIT2</b> method gets the event information table (EIT).

## -parameters

### -param tableId [in]

Specifies the table identifier of the EIT. Use one of the following values.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVB_EIT_ACTUAL_TID"></a><a id="dvb_eit_actual_tid"></a><dl>
<dt><b>DVB_EIT_ACTUAL_TID</b></dt>
<dt> 0x4E</dt>
</dl>
</td>
<td width="60%">
Present/following EIT for this transport stream.

</td>
</tr>
<tr>
<td width="40%"><a id="DVB_EIT_OTHER_TID_"></a><a id="dvb_eit_other_tid_"></a><dl>
<dt><b>DVB_EIT_OTHER_TID </b></dt>
<dt>0x4F</dt>
</dl>
</td>
<td width="60%">
Present/following EIT for another transport stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x50 – 0x5F</dt>
</dl>
</td>
<td width="60%">
Schedule EIT for this transport stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x60 – 0x6F</dt>
</dl>
</td>
<td width="60%">
Schedule EIT for another transport stream.

</td>
</tr>
</table>

### -param pwServiceId [in]

An optional parameter that contains a service identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.

### -param pbSegment [in]

An optional parameter that contains a segment number. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.

### -param ppEIT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit2">IDVB_EIT2</a> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive the table in the allotted time.

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

## -remarks

The method fails if the filter does not receive a matching table within a predetermined length of time.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser2">IDvbSiParser2</a>