---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRDPSRAPIVirtualChannel::SendData


## -description


Sends data on the channel.


## -parameters




### -param bstrData [in]

Type: <b>BSTR</b>

The buffer to be sent in a packet on the channel. The maximum size  of the data is CONST_MAX_MESSAGE_SIZE bytes.


### -param lAttendeeId [in]

Type: <b>long</b>

The attendee that should receive the data. To send the data to all attendees, use CONST_ATTENDEE_ID_EVERYONE.


### -param ChannelSendFlags [in]

Type: <b>unsigned long</b>

The channel flags. This parameter can be 0 or the following value.



#### CHANNEL_FLAGS_UNCOMPRESSED

The data should not be compressed before it is sent because it is in a format that is already compressed.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/c3cceb22-424d-4ed9-8d4d-0ca523ba5e9c">IRDPSRAPIVirtualChannel</a>
 

 

