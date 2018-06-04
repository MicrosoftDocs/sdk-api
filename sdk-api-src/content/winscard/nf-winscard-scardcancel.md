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

# SCardCancel function


## -description


The <b>SCardCancel</b> function terminates all outstanding actions within a specific <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>.

The only requests that you can cancel are those that require waiting for external action by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> or user. Any such outstanding action requests will terminate with a status indication that the action was canceled. This is especially useful to force outstanding <a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a> calls to terminate.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


## -returns



This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>SCardCancel</b> function is a smart card tracking function. For a description of other tracking functions, see 
<a href="https://msdn.microsoft.com/b26b26bf-85ff-435f-a679-7529f19b1c1b">Smart Card Tracking Functions</a>.


#### Examples

The following example cancels all outstanding actions in the specified context.  The example assumes that lReturn is an existing variable of type <b>LONG</b> and that hContext is a valid handle received from a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
lReturn = SCardCancel( hContext );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardCancel\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a>



<a href="https://msdn.microsoft.com/7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0">SCardLocateCards</a>
 

 

