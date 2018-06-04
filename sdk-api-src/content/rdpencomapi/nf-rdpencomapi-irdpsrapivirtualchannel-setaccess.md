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

# IRDPSRAPIVirtualChannel::SetAccess


## -description


Enables the channel for an attendee.


## -parameters




### -param lAttendeeId [in]

Type: <b>long</b>

The identifier of the attendee.


### -param AccessType [in]

Type: <b>CHANNEL_ACCESS_ENUM</b>

The type of access granted. This parameter can be one of the following values.

<a id="CHANNEL_ACCESS_ENUM_NONE"></a>
<a id="channel_access_enum_none"></a>


#### CHANNEL_ACCESS_ENUM_NONE

<a id="CHANNEL_ACCESS_ENUM_SENDRECEIVE"></a>
<a id="channel_access_enum_sendreceive"></a>


#### CHANNEL_ACCESS_ENUM_SENDRECEIVE


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -remarks



This method must be called for each attendee that will receive data over the channel.




## -see-also




<a href="https://msdn.microsoft.com/c3cceb22-424d-4ed9-8d4d-0ca523ba5e9c">IRDPSRAPIVirtualChannel</a>
 

 

