---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber
title: IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber (dvbsiparser.h)
description: Gets the value of the logical_channel_number field from a Digital Video Broadcast (DVB) logical channel descriptor. The logical_channel_number field gives the ordinal position of the service record in the descriptor.
helpviewer_keywords: ["GetListRecordLogicalChannelNumber","GetListRecordLogicalChannelNumber method [Microsoft TV Technologies]","GetListRecordLogicalChannelNumber method [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","GetListRecordLogicalChannelNumber method","IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber","IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber","dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber","mstv.idvblogicalchannel2descriptor_getlistrecordlogicalchannelnumber"]
old-location: mstv\idvblogicalchannel2descriptor_getlistrecordlogicalchannelnumber.htm
tech.root: mstv
ms.assetid: b8ebc804-08a1-4840-ba20-f52438a0d6bf
ms.date: 12/05/2018
ms.keywords: GetListRecordLogicalChannelNumber, GetListRecordLogicalChannelNumber method [Microsoft TV Technologies], GetListRecordLogicalChannelNumber method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListRecordLogicalChannelNumber method, IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber, IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber, mstv.idvblogicalchannel2descriptor_getlistrecordlogicalchannelnumber
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber
 - dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber
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
 - IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber
---

# IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the logical_channel_number field from a Digital Video Broadcast (DVB) logical channel descriptor. The logical_channel_number field gives the ordinal position of the service record in the descriptor.

## -parameters

### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getcountoflists">IDvbLogicalChannel2Descriptor::GetCountOfLists</a> method to get the number of channel list records in the logical channel descriptor.

### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a> method to get the number of service records in the logical channel descriptor.

### -param pwVal [out]

Receives the logical channel number. This can be any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Service not suitable for user selection

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1 - 999</dt>
</dl>
</td>
<td width="60%">
Logical channel number

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000 - 1023</dt>
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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getcountoflists">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>