---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CAPABILITY_ALLOW0_
title: FWPM_NET_EVENT_CAPABILITY_ALLOW0_
author: windows-sdk-content
description: Contains information about network traffic allowed in relation to an app container network capability.
old-location: fwp\fwpm_net_event_capability_allow0.htm
old-project: FWP
ms.assetid: e53e92e5-f7fa-4457-8681-754b50b24273
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_NET_EVENT_CAPABILITY_ALLOW0, FWPM_NET_EVENT_CAPABILITY_ALLOW0 structure [Filtering], FWPM_NET_EVENT_CAPABILITY_ALLOW0_, fwp.fwpm_net_event_capability_allow0, fwpmtypes/FWPM_NET_EVENT_CAPABILITY_ALLOW0
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FWPM_NET_EVENT_CAPABILITY_ALLOW0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_CAPABILITY_ALLOW0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_CAPABILITY_ALLOW0_ structure


## -description


The <b>FWPM_NET_EVENT_CAPABILITY_ALLOW0</b> structure contains information about network traffic allowed in relation to an app container network capability.. The specified app container network capability grants access to network resources, and  the specified filter identifier enforces allowing access.


## -struct-fields




### -field networkCapabilityId

Type: <b><a href="https://msdn.microsoft.com/e69ac412-0868-49da-9a87-58a03098839d">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a></b>

The specific app container network capability allowing this traffic.


### -field filterId

Type: <b>UINT64</b>

A LUID identifying the WFP filter enforcing the allowed access intended by the capability in <b>networkCapabilityId</b>.


### -field isLoopback

Type: <b>BOOL</b>

True if the packet originated from (or was heading to) the loopback adapter; otherwise, false.


## -see-also




<a href="https://msdn.microsoft.com/e69ac412-0868-49da-9a87-58a03098839d">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a>



<a href="https://msdn.microsoft.com/40848332-0961-417c-8adc-dd1a380594ba">FWPM_NET_EVENT_CAPABILITY_DROP0</a>
 

 

