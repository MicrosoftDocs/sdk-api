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

# ISettingsContext::GetNamespaces


## -description


Gets the namespaces that exist in the context.


## -parameters




### -param ppNamespaceIds [out]

An <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> interface pointer that represents the collection of namespaces.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -remarks



<div class="alert"><b>Note</b>  This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources in the system to allocate a new enumerator.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

