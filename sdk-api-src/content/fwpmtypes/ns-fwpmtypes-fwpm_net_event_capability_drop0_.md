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

# FWPM_NET_EVENT_CAPABILITY_DROP0_ structure


## -description


The <b>FWPM_NET_EVENT_CAPABILITY_DROP0</b> structure contains information about network traffic dropped  in relation to an app container network capability. Traffic is dropped due to the specified app container network capability and enforced by  the specified filter identifier.


## -struct-fields




### -field networkCapabilityId

Type: <b><a href="https://msdn.microsoft.com/e69ac412-0868-49da-9a87-58a03098839d">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a></b>

The specific app container network capability which was missing, therefore causing this traffic to be denied.


### -field filterId

Type: <b>UINT64</b>

A LUID identifying the WFP filter where the traffic drop occurred.


### -field isLoopback

Type: <b>BOOL</b>

True if the packet originated from (or was heading to) the loopback adapter; otherwise, false.


## -see-also




<a href="https://msdn.microsoft.com/e69ac412-0868-49da-9a87-58a03098839d">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a>



<a href="https://msdn.microsoft.com/e53e92e5-f7fa-4457-8681-754b50b24273">FWPM_NET_EVENT_CAPABILITY_ALLOW0</a>
 

 

