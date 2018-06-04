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

# ISettingsEngine::GetNamespaces


## -description


Returns an enumerator to the installed namespaces.


## -parameters




### -param Flags [in]

A <a href="https://msdn.microsoft.com/606fad95-1f93-4e16-9be5-2ebd52b91180">WcmNamespaceEnumerationFlags</a> value that specifies the context to include in the collection of namespaces.


### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param Namespaces [out]

An <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> interface pointer whose methods can be used to access members of the collection.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_USERNOTFOUND</b> if the store is not loaded.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

