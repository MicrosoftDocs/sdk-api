---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK1
title: FWPM_NET_EVENT_CALLBACK1
author: windows-driver-content
description: Is used to add custom behavior to the net event subscription process.
old-location: fwp\fwpm_net_event_callback1.htm
old-project: FWP
ms.assetid: fddf8e2e-e133-4575-a6dc-c7b5e6cfff31
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FWPM_NET_EVENT_CALLBACK1, FWPM_NET_EVENT_CALLBACK1 callback, FWPM_NET_EVENT_CALLBACK1 callback function [Filtering], fwp.fwpm_net_event_callback1, fwpmu/FWPM_NET_EVENT_CALLBACK1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	fwpmu.h
api_name:
-	FWPM_NET_EVENT_CALLBACK1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_CALLBACK1 callback function


## -description


The <b>FWPM_NET_EVENT_CALLBACK1</b> function is used to add custom behavior to the net event subscription process.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CALLBACK1</b> is the specific implementation of FWPM_NET_EVENT_CALLBACK used in Windows 8 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/69b311c5-ac08-490b-823b-4049f7c46975">FWPM_NET_EVENT_CALLBACK0</a> is available.</div><div> </div>

## -parameters




### -param *context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/1e079574-3ab0-48d4-84ab-b2b3f34f757b">FwpmNetEventSubscribe1</a> function.


### -param *event [in]

Type: <b>const <a href="https://msdn.microsoft.com/fbcacfb1-b471-474e-bdee-12a481fadc63">FWPM_NET_EVENT2</a>*</b>

The net event information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/1e079574-3ab0-48d4-84ab-b2b3f34f757b">FwpmNetEventSubscribe1</a> to register this callback function.



