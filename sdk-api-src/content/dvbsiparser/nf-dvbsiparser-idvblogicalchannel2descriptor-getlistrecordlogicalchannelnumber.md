---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber
title: IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber
author: windows-sdk-content
description: Gets the value of the logical_channel_number field from a Digital Video Broadcast (DVB) logical channel descriptor. The logical_channel_number field gives the ordinal position of the service record in the descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistrecordlogicalchannelnumber.htm
old-project: mstv
ms.assetid: b8ebc804-08a1-4840-ba20-f52438a0d6bf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetListRecordLogicalChannelNumber, GetListRecordLogicalChannelNumber method [Microsoft TV Technologies], GetListRecordLogicalChannelNumber method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListRecordLogicalChannelNumber method, IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber, IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber, mstv.idvblogicalchannel2descriptor_getlistrecordlogicalchannelnumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelNumber


## -description


Gets the value of the logical_channel_number field from a Digital Video Broadcast (DVB) logical channel descriptor. The logical_channel_number field gives the ordinal position of the service record in the descriptor.


## -parameters




### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/13a439d1-c6b6-49ab-a41e-caa27e320f37">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>method to get the number of channel list records in the logical channel descriptor.


### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>method to get the number of service records in the logical channel descriptor.



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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc60db7f-ae49-48dd-bd8a-62899e5ca7a3">IDvbLogicalChannel2Descriptor</a>



<a href="https://msdn.microsoft.com/13a439d1-c6b6-49ab-a41e-caa27e320f37">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>



<a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>
 

 

