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

# _MFPOLICYMANAGER_ACTION enumeration


## -description



Defines actions that can be performed on a stream.




## -enum-fields




### -field PEACTION_NO

No action.


### -field PEACTION_PLAY

Play the stream.


### -field PEACTION_COPY

Copy the stream.


### -field PEACTION_EXPORT

Export the stream to another format.


### -field PEACTION_EXTRACT

Extract the data from the stream and pass it to the application. For example, acoustic echo cancellation requires this action.


### -field PEACTION_RESERVED1

Reserved.


### -field PEACTION_RESERVED2

Reserved.


### -field PEACTION_RESERVED3

Reserved.


### -field PEACTION_LAST

Last member of the enumeration.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

