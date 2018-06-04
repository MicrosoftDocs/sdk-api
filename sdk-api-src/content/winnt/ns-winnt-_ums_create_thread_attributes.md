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

# _UMS_CREATE_THREAD_ATTRIBUTES structure


## -description


Specifies attributes for a user-mode scheduling (UMS) worker thread. 

This structure is used with the <a href="https://msdn.microsoft.com/5fc3e04f-9b2a-440c-a9aa-d78d9b25b341">UpdateProcThreadAttribute</a> function.  


## -struct-fields




### -field UmsVersion

The UMS version for which the application was built. This parameter must be <b>UMS_VERSION</b>. 


### -field UmsContext

A pointer to a UMS thread context for the worker thread to be created. This pointer is provided by the <a href="https://msdn.microsoft.com/b27ce81a-8463-46af-8acf-2de091f625df">CreateUmsThreadContext</a> function.


### -field UmsCompletionList

A pointer to a UMS completion list. This pointer is provided by the <a href="https://msdn.microsoft.com/6e77b793-a82e-4e23-8c8b-7aff79d69346">CreateUmsCompletionList</a> function. The newly created worker thread is queued to the specified completion list.

