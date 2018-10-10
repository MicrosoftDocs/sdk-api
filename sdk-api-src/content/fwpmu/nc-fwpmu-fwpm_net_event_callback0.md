---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK0
title: FWPM_NET_EVENT_CALLBACK0
author: windows-sdk-content
description: Is used to add custom behavior to the net event subscription process.
old-location: fwp\fwpm_net_event_callback0_func.htm
tech.root: FWP
ms.assetid: 69b311c5-ac08-490b-823b-4049f7c46975
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FWPM_NET_EVENT_CALLBACK0, FWPM_NET_EVENT_CALLBACK0 callback, FWPM_NET_EVENT_CALLBACK0 callback function [Filtering], fwp.fwpm_net_event_callback0_func, fwpmu/FWPM_NET_EVENT_CALLBACK0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - FWPM_NET_EVENT_CALLBACK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FWPM_NET_EVENT_CALLBACK0 callback function


## -description


The <b>FWPM_NET_EVENT_CALLBACK0</b> function is used to add custom behavior to the net event subscription process.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CALLBACK0</b> is the specific implementation of FWPM_NET_EVENT_CALLBACK used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/fddf8e2e-e133-4575-a6dc-c7b5e6cfff31">FWPM_NET_EVENT_CALLBACK1</a> is available.</div><div> </div>

## -parameters




### -param *context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/a2671600-c231-46c8-966d-f444fbdfa944">FwpmNetEventSubscribe0</a> function.


### -param *event [in]

Type: <b>const <a href="https://msdn.microsoft.com/0f989f66-8373-4546-ade3-8b337c4507e2">FWPM_NET_EVENT1</a>*</b>

The net event information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/a2671600-c231-46c8-966d-f444fbdfa944">FwpmNetEventSubscribe0</a> to register this callback function.




## -see-also




<a href="https://msdn.microsoft.com/0f989f66-8373-4546-ade3-8b337c4507e2">FWPM_NET_EVENT1</a>



<a href="https://msdn.microsoft.com/a2671600-c231-46c8-966d-f444fbdfa944">FwpmNetEventSubscribe0</a>
 

 

