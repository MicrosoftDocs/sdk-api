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

# IDirectInputJoyConfig8::AddRef


## -description


The <b>IDirectInputJoyConfig8::AddRef</b> method increases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 


## -parameters






## -returns



Returns the new reference count of the object.




## -remarks



When the DirectInputJoyConfig object is created, its reference count should be set to 1. Every time an application obtains an interface to the object or calls the <b>AddRef</b> method, the object's reference count is increased by 1. The application uses the <b>Release</b> method to decrease the reference count of the object by 1.



