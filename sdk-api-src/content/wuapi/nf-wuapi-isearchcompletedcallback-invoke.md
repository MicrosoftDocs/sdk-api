---
UID: NF:wuapi.ISearchCompletedCallback.Invoke
title: ISearchCompletedCallback::Invoke
author: windows-sdk-content
description: Handles the notification of the completion of an asynchronous search that is initiated by calling the IUpdateSearcher.BeginSearch method.
old-location: wua\isearchcompletedcallback_invoke.htm
old-project: Wua_Sdk
ms.assetid: 2d06754a-5750-4986-9f54-98f91dcc705b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISearchCompletedCallback interface [Windows Update Agent],Invoke method, ISearchCompletedCallback.Invoke, ISearchCompletedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],ISearchCompletedCallback interface, wua.isearchcompletedcallback_invoke, wuapi/ISearchCompletedCallback::Invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - ISearchCompletedCallback.Invoke
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

