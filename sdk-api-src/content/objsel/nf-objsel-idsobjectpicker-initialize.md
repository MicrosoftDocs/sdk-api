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

# IDsObjectPicker::Initialize


## -description


The <b>IDsObjectPicker::Initialize</b> method initializes the object picker dialog box with data about the scopes, filters, and options used by the object picker dialog box.


## -parameters




### -param pInitInfo

Pointer to a 
<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a> structure that contains the initialization data.


## -returns



Returns a standard error code or one of the following values.




## -remarks



<b>IDsObjectPicker::Initialize</b> can be called more than once and the last call takes precedence. The <a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a> object will completely re-initialize itself in response  to this method.




## -see-also




<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a>
 

 

