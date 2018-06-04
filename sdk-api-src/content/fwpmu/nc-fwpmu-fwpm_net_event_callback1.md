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



