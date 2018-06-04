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

# AM_WMT_EVENT_DATA structure


## -description



The AM_WMT_EVENT_DATA structure contains information pertaining to a <a href="https://msdn.microsoft.com/ac6ea7a1-238e-42ae-9f10-e1db60381357">EC_WMT_EVENT</a> event.




## -struct-fields




### -field hrStatus

The status code returned by the Windows Media Format SDK.


### -field pData

Pointer whose data is dependent on the value of the <a href="https://msdn.microsoft.com/ebf77e8a-65e8-4da9-bb21-a1e2bf427bbf">WMT_STATUS</a> message in <i>lParam1</i> of the <a href="https://msdn.microsoft.com/ac6ea7a1-238e-42ae-9f10-e1db60381357">EC_WMT_EVENT</a> event.


## -remarks



This structure is relevant when using the <a href="https://msdn.microsoft.com/82b9f849-b9dc-439b-8ca7-9dcd992338ab">WM ASF Reader</a> filter to read files protected with Digital Rights Management.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

