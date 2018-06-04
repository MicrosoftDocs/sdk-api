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

# _BTH_QUERY_DEVICE structure


## -description


The 
<b>BTH_QUERY_DEVICE</b> structure is used when querying for the presence of a Bluetooth device.


## -struct-fields




### -field LAP

Reserved. Must be set to zero.


### -field length

Requested length of the inquiry, in seconds.


## -remarks



See the Bluetooth specification at 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84017">www.bluetooth.com</a> for additional information about LAP.




## -see-also




<a href="https://msdn.microsoft.com/32fa710f-8645-4cf3-a882-cc032d66d979">Bluetooth and WSALookupServiceBegin for Device
		  Inquiry</a>



<a href="https://msdn.microsoft.com/0c0d26f7-b6c3-42a9-8c01-118278c381cc">Bluetooth and WSAQUERYSET for Device Inquiry</a>
 

 

