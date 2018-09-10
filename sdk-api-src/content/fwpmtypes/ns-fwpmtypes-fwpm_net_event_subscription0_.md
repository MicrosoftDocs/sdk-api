---
UID: NS:fwpmtypes.FWPM_NET_EVENT_SUBSCRIPTION0_
title: FWPM_NET_EVENT_SUBSCRIPTION0_
author: windows-sdk-content
description: Stores information used to subscribe to notifications about a network event.
old-location: fwp\fwpm_net_event_subscription0.htm
tech.root: fwp
ms.assetid: a1aa8369-fd70-46f6-983d-0afdf8b8ff77
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FWPM_NET_EVENT_SUBSCRIPTION0, FWPM_NET_EVENT_SUBSCRIPTION0 structure [Filtering], FWPM_NET_EVENT_SUBSCRIPTION0_, fwp.fwpm_net_event_subscription0, fwpmtypes/FWPM_NET_EVENT_SUBSCRIPTION0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - FWPM_NET_EVENT_SUBSCRIPTION0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_SUBSCRIPTION0
req.redist: 
---

# FWPM_NET_EVENT_SUBSCRIPTION0_ structure


## -description


The <b>FWPM_NET_EVENT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a network event.


## -struct-fields




### -field enumTemplate

Address of an <a href="https://msdn.microsoft.com/79711b24-e092-4a36-810a-6acad279eb90">FWPM_NET_EVENT_ENUM_TEMPLATE0</a> structure. Notifications are only dispatched for objects that match the template. If
   <b>enumTemplate</b> is <b>NULL</b>, it matches all objects.


### -field flags

Unused.


### -field sessionKey

Identifies the session which created the subscription.


## -remarks



<b>FWPM_NET_EVENT_SUBSCRIPTION0</b> is a specific implementation of FWPM_NET_EVENT_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.



