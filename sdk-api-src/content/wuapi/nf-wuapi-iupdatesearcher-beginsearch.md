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

# IUpdateSearcher::BeginSearch


## -description


Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.


## -parameters




### -param criteria [in]

A string that specifies the search criteria.


### -param onCompleted [in]

An <a href="https://msdn.microsoft.com/f228808d-7f7e-4107-a4b6-4bac5b48d1b4">ISearchCompletedCallback</a> interface that is called when an asynchronous search operation is complete.


### -param state [in]

The caller-specific  state that is returned by the <a href="https://msdn.microsoft.com/68d861a3-420d-4a89-ac32-900db6d51036">AsyncState</a> property of the <a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a> interface.


### -param retval [out]

An <a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a> interface that represents the current operation that might be pending. 

The caller passes the returned value to the <a href="https://msdn.microsoft.com/4a0532ec-3613-4aa1-96d7-7291b9ca7a94">EndSearch</a> method to complete a search operation.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
</table>
 




## -remarks



For a complete description of search criteria syntax, see <a href="https://msdn.microsoft.com/library/windows/hardware/mt219145">Search</a>.

  As an alternative to implementing the <a href="https://msdn.microsoft.com/f228808d-7f7e-4107-a4b6-4bac5b48d1b4">ISearchCompletedCallback</a> interface, you can use a script to   implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the <i>onCompleted</i> parameter is <b>IUnknown*</b>.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 

