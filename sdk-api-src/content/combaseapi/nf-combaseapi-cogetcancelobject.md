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

# CoGetCancelObject function


## -description


Obtains a pointer to a call control interface, normally <a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>, on the cancel object corresponding to an outbound COM method call pending on the same or another client thread.


## -parameters




### -param dwThreadId [in]

The identifier of the thread on which the pending COM call is to be canceled. If this parameter is 0, the call is on the current thread.


### -param iid [in]

The globally unique identifier of an interface on the cancel object for the call to be canceled. This argument is usually IID_ICancelMethodCalls.


### -param ppUnk [out]

Receives the address of a pointer to the interface specified by <i>riid</i>.


## -returns



This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call control object was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object on which the call is executing does not support the interface specified by <i>riid</i>.

</td>
</tr>
</table>
 




## -remarks



If two or more calls are pending on the same thread through nested calls, the thread ID may not be sufficient to identify the call to be canceled. In this case, <b>CoGetCancelObject</b> returns a cancel interface corresponding to the innermost call that is pending on the thread and has registered a cancel object.

This function does not locate cancel objects for asynchronous calls.



