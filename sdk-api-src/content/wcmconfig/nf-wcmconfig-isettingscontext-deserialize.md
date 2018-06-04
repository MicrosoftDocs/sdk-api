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

# ISettingsContext::Deserialize


## -description


Deserializes the data in the stream that is provided to this context.


## -parameters




### -param pStream [in]

A pointer to an IStream initialized stream object containing the XML representing a settings section of an answer (Unattend.xml) file.
An answers file is a file that facilitates the unattend process during setup or migration  to execute all of its tasks automatically, without user intervention.


### -param pTarget [in]

A pointer that identifies <a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a> target object that should be used while deserializing the stream. This target should match the target which will be used on the engine alongside this context.


### -param pppResults [out]

A pointer to an array of <a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a> interface pointers. Each interface pointer identifies an issue which may have occurred during deserialization.




### -param pcResultCount [out]

The number of ISettingsResult objects in the array pppResults.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_NAMESPACENOTFOUND</b> if pIdentity references a namespace that is not in the context.

This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources on the system to allocate the enumerators.




## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

