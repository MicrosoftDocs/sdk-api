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

# _FILESHARE_CHANGE structure


## -description


Describes the format for an entry in an event notification list.


## -struct-fields




### -field Change

Describes a change event. This value is taken from the 
       <a href="https://msdn.microsoft.com/36139a95-141c-4f44-9627-9ed6c3fed0c5">FILESHARE_CHANGE_ENUM</a>enumeration. The following 
       are the possible values for this member.



#### FILESHARE_CHANGE_ADD (1)

A new file share resource has been created and will be included with the other file shares managed by the 
         File Server resource.



#### FILESHARE_CHANGE_DEL (2)

A file share resource has been deleted and will be removed from the file shares managed by the File Server 
         resource.



#### FILESHARE_CHANGE_MODIFY (3)

One or more properties of an existing file share resource have been changed.


### -field ShareName

The name of the file share resource specific to this entry in the event notification list.


## -see-also




<a href="https://msdn.microsoft.com/36139a95-141c-4f44-9627-9ed6c3fed0c5">FILESHARE_CHANGE_ENUM</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

