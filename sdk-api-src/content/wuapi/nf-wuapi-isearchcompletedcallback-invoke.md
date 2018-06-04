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

# ISearchCompletedCallback::Invoke


## -description


Handles the notification of the completion of an asynchronous search that is initiated by calling the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">IUpdateSearcher.BeginSearch</a> method.


## -parameters




### -param searchJob [in]

An <a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a> interface that contains search information.


### -param callbackArgs [in]

This parameter is reserved for future use and can be ignored. An <a href="https://msdn.microsoft.com/809e4a09-3ad8-4e7f-8ace-ae613d05a7e1">ISearchCompletedCallbackArgs</a> interface that contains information on the completion of an asynchronous search.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/f228808d-7f7e-4107-a4b6-4bac5b48d1b4">ISearchCompletedCallback</a>



<a href="https://msdn.microsoft.com/2d06754a-5750-4986-9f54-98f91dcc705b">IUpdateSearcher::BeginSearch</a>
 

 

