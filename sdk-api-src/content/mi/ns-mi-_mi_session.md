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

# _MI_Session structure


## -description


An object that is associated with a destination and has a set of credentials and options associated with it. .


## -struct-fields




### -field reserved1

For internal use only.


### -field reserved2

For internal use only.


### -field ft

This is the function table for accessing carrying out 
                      operations on a destination machine, along with configuration of the session. Use the functions containing the MI_Session_ prefix to access this information.


## -see-also




<a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>



<a href="https://msdn.microsoft.com/275657b1-9e74-456e-9ef9-28b621d27fc7">MI_Context_GetLocalSession</a>
 

 

