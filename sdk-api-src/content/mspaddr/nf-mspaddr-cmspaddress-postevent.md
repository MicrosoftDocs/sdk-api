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

# CMSPAddress::PostEvent


## -description


The 
<b>PostEvent</b> method is called by the MSPCall to post an event to TAPI3. This method puts the event at the end of the event list and signals TAPI3. Locks the event list.


## -parameters




### -param EventItem [in]

Pointer to the 
<a href="https://msdn.microsoft.com/fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc">MSPEVENTITEM</a> structure, which contains the event information.


## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

