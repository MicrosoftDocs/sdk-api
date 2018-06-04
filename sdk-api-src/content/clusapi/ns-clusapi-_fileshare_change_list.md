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

# _FILESHARE_CHANGE_LIST structure


## -description


Describes an event notification list for file shares managed by the File Server 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -struct-fields




### -field NumEntries

The number of entries the event notification list contains.


### -field ChangeEntry

An entry in the event notification list. The format of this member comes from the 
       <a href="https://msdn.microsoft.com/f317f162-49b2-43df-a298-e2de707e089a">FILESHARE_CHANGE</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/f317f162-49b2-43df-a298-e2de707e089a">FILESHARE_CHANGE</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

