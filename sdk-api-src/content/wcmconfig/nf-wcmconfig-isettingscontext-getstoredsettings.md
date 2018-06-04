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

# ISettingsContext::GetStoredSettings


## -description


Gets the stored setting changes from the context for the given namespace. This method returns a pointer to an address of an enumerator for each of the parameters <i>ppAddedSettings</i>, <i>ppModifiedSettings</i>, and <i>ppDeletedSettings</i> that identifies the set of paths for the added, modified, and deleted settings respectively. These strings may then be passed to <a href="https://msdn.microsoft.com/11f541e6-fd97-4756-91c1-44ba2e3d35b1">ISettingsContext::RevertSetting</a>.


## -parameters




### -param pIdentity [in]

The <a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a> object that specifies the namespace to get the settings for. This namespace identity should be fully-specified.


### -param ppAddedSettings [out]

 A pointer to a newly allocated <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that lists the set of paths for the added settings. Each path identifies a setting added to the context. 


### -param ppModifiedSettings [out]

A pointer to a newly-allocated <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that lists the set of paths for the modified settings.


### -param ppDeletedSettings [out]

A pointer to a newly-allocated <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that lists the set of paths for the deleted settings.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_NAMESPACENOTFOUND</b> if <i>pIdentity</i> references a namespace that is not in the context.

It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources on the system to allocate the enumerators.




## -remarks



<i>ppAddedSettings</i>, <i>ppModifiedSettings</i>, and <i>ppDeletedSettings</i> are enumerators for which Current returns a var with variable type BSTR that identifies the paths for the added, modified, and deleted settings respectively. Enumerating through the enumerators produces a set of path strings, each of which identifies a setting that has been added, modified, or deleted in this context. These strings can then be passed to <a href="https://msdn.microsoft.com/11f541e6-fd97-4756-91c1-44ba2e3d35b1">RevertSetting</a>.




## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

