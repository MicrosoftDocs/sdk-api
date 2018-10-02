---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelAndVisibility
title: IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelAndVisibility
author: windows-sdk-content
description: Gets the visible_service_flag and logical_channel_number fields from a Digital Video Broadcast (DVB) logical channel descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistrecordlogicalchannelandvisibility.htm
tech.root: MSTV
ms.assetid: 1e9d5d7f-4816-4eb8-894a-85dd7977c62e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetListRecordLogicalChannelAndVisibility, GetListRecordLogicalChannelAndVisibility method [Microsoft TV Technologies], GetListRecordLogicalChannelAndVisibility method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListRecordLogicalChannelAndVisibility method, IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelAndVisibility, IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelAndVisibility, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelAndVisibility, mstv.idvblogicalchannel2descriptor_getlistrecordlogicalchannelandvisibility, mstv.idvblogicalchanneldescriptor2_getlistrecordlogicalchannelandvisibility
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbLogicalChannel2Descriptor.GetListRecordLogicalChannelAndVisibility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbLogicalChannel2Descriptor::GetListRecordLogicalChannelAndVisibility


## -description


Gets the visible_service_flag and logical_channel_number fields from a Digital Video Broadcast (DVB) logical channel descriptor.  The visible_service_flag indicates whether a service record in the DVB logical channel descriptor is visible through the receiver service list and can be selected. The logical_channel_number field contains a broadcaster-defined channel number that is used to order services. 


## -parameters




### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/13a439d1-c6b6-49ab-a41e-caa27e320f37">GetCountOfLists</a>method to get the number of channel list records in the logical channel descriptor.


### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">GetListCountOfRecords</a>method to get the number of service records in the logical channel descriptor.



### -param pwVal [out]

Receives the visible_service_flag (defined by bit 15) and logical_channel_number (defined by bits 0 - 9) field values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The combinations of visible_service_flag and local_channel_number field values have the following meanings.

<table>
<tr>
<th>visible_service_flag</th>
<th>logical_channel_number</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>0</td>
<td>  Service not suitable for selection by the user. For example, the value zero may
be used for data services intended only for selection from interactive
applications or for firmware download services.</td>
</tr>
<tr>
<td>1</td>
<td>0</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>0</td>
<td>1-1024</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>1</td>
<td>1-999</td>
<td>Service is displayed in service lists and Event Schedule Guide (ESG). Service is accessible via P+/- keys or from
numeric keys (same value as decimal value of logical_channel_number).</td>
</tr>
<tr>
<td>1</td>
<td>&gt; 999</td>
<td>Reserved.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/13a439d1-c6b6-49ab-a41e-caa27e320f37">GetCountOfLists</a>



<a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">GetListCountOfRecords</a>



<a href="https://msdn.microsoft.com/dc60db7f-ae49-48dd-bd8a-62899e5ca7a3">IDvbLogicalChannel2Descriptor</a>
 

 

