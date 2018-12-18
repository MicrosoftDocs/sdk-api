---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CAPABILITY_DROP0_
title: FWPM_NET_EVENT_CAPABILITY_DROP0
author: windows-sdk-content
description: Contains information about network traffic dropped in relation to an app container network capability.
old-location: fwp\fwpm_net_event_capability_drop0.htm
tech.root: fwp
ms.assetid: 40848332-0961-417c-8adc-dd1a380594ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_NET_EVENT_CAPABILITY_DROP0, FWPM_NET_EVENT_CAPABILITY_DROP0 structure [Filtering], fwp.fwpm_net_event_capability_drop0, fwpmtypes/FWPM_NET_EVENT_CAPABILITY_DROP0
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_CAPABILITY_DROP0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_CAPABILITY_DROP0
req.redist: 
---

# FWPM_NET_EVENT_CAPABILITY_DROP0 structure


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
 

 

