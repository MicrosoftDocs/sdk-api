---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK2
title: FWPM_NET_EVENT_CALLBACK2
author: windows-sdk-content
description: Is used to add custom behavior to the net event subscription process.
old-location: fwp\fwpm_net_event_callback2.htm
old-project: FWP
ms.assetid: 0A5E0ADB-0879-4646-9F69-D8AB9BD067AD
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_NET_EVENT_CALLBACK2, FWPM_NET_EVENT_CALLBACK2 callback, FWPM_NET_EVENT_CALLBACK2 callback function [Filtering], fwp.fwpm_net_event_callback2, fwpmu/FWPM_NET_EVENT_CALLBACK2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - fwpmu.h
api_name:
 - FWPM_NET_EVENT_CALLBACK2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_CALLBACK2 callback function


## -description


The <b>FWPM_NET_EVENT_CALLBACK2</b> function is used to add custom behavior to the net event subscription process.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CALLBACK2</b> is the specific implementation of FWPM_NET_EVENT_CALLBACK used in Windows 10, version 1607 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/fddf8e2e-e133-4575-a6dc-c7b5e6cfff31">FWPM_NET_EVENT_CALLBACK1</a> is available. For Windows 7, <a href="https://msdn.microsoft.com/69b311c5-ac08-490b-823b-4049f7c46975">FWPM_NET_EVENT_CALLBACK0</a> is available.</div><div> </div>

## -parameters




### -param *context [in, out]

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/CC55CA33-A153-4B48-AA89-A28F010024F7">FwpmNetEventSubscribe2</a> function.


### -param *event [in]

The net event information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/CC55CA33-A153-4B48-AA89-A28F010024F7">FwpmNetEventSubscribe2</a> to register this callback function.




## -see-also




<a href="https://msdn.microsoft.com/CC55CA33-A153-4B48-AA89-A28F010024F7">FwpmNetEventSubscribe2</a>
 

 

