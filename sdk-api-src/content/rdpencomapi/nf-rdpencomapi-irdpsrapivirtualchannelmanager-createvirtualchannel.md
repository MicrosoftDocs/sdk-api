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

# IRDPSRAPIVirtualChannelManager::CreateVirtualChannel


## -description


Creates a virtual channel.


## -parameters




### -param bstrChannelName [in]

Type: <b>BSTR</b>

The name of the channel. The maximum length is 8 characters, including the null-terminating character. Legacy channel names are limited to 32 characters.


### -param Priority [in]

Type: <b>CHANNEL_PRIORITY</b>

The priority of the channel. This parameter can be one of the following values.

<a id="CHANNEL_PRIORITY_LO"></a>
<a id="channel_priority_lo"></a>


#### CHANNEL_PRIORITY_LO

<a id="CHANNEL_PRIORITY_MED"></a>
<a id="channel_priority_med"></a>


#### CHANNEL_PRIORITY_MED

<a id="CHANNEL_PRIORITY_HI"></a>
<a id="channel_priority_hi"></a>


#### CHANNEL_PRIORITY_HI


### -param ChannelFlags [in]

Type: <b>unsigned long</b>

Flags that determine how data is sent on the channel. This parameter can be 0 or <a href="https://msdn.microsoft.com/ca8a063a-81a0-44b8-8654-36a38a6f30ef">CHANNEL_FLAGS_UNCOMPRESSED</a>.


### -param ppChannel [out]

Type: <b>IRDPSRAPIVirtualChannel**</b>

An <a href="https://msdn.microsoft.com/c3cceb22-424d-4ed9-8d4d-0ca523ba5e9c">IRDPSRAPIVirtualChannel</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code. The following is a possible value.




## -remarks



When a virtual channel is created, an RDP virtual channel is bound at the RDP stack layer for each opened channel. For a channel to actually be opened between the client and the server, both the client and the server have to bind the channel. The <i>Priority</i> parameter is used to assign a priority to the packets send on the channel.

The binding between server and client channels is established based on the channel name.




## -see-also




<a href="https://msdn.microsoft.com/750e7d98-196f-4bf2-864b-50b3bef6f6ad">IRDPSRAPIVirtualChannelManager</a>
 

 

