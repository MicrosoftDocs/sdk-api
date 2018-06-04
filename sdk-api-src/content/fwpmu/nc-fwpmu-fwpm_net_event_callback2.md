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
 

 

