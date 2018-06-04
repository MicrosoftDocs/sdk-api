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

# lpminitinfo structure


## -description


The 
<b>LPM_INIT_INFO</b> structure contains local policy module initialization information.


## -struct-fields




### -field PcmVersionNumber

Version of the policy control module


### -field ResultTimeLimit

Time limit, in seconds, that the policy control module waits to receive results before timing out. 


### -field ConfiguredLpmCount

Number of configured local policy modules.


### -field AllocMemory

Memory allocation function used to initialize memory for local policy modules, in the form of a <a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a> function.


### -field FreeMemory

Memory freeing function used to free memory allocated for the local policy module.  See <a href="https://msdn.microsoft.com/b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037">PFREEMEM</a> for more information.


### -field PcmAdmitResultCallback

Callback function used to admit results. See <a href="https://msdn.microsoft.com/9040155b-6c6d-4deb-a63a-74e5fc8123ba">cbAdmitResult</a> for more information.


### -field GetRsvpObjectsCallback

Callback function used to obtain RSVP objects. See <a href="https://msdn.microsoft.com/baedb3e9-7768-4666-8bd7-78dd1d0eb0de">cbGetRsvpObjects</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>



<a href="https://msdn.microsoft.com/b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037">PFREEMEM</a>



<a href="https://msdn.microsoft.com/9040155b-6c6d-4deb-a63a-74e5fc8123ba">cbAdmitResult</a>



<a href="https://msdn.microsoft.com/baedb3e9-7768-4666-8bd7-78dd1d0eb0de">cbGetRsvpObjects</a>
 

 

