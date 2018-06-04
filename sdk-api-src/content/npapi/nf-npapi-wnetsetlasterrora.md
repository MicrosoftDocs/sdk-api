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

# WNetSetLastErrorA function


## -description


Sets extended error information. Network providers should call this function instead of 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>.

When necessary, the <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Multiple Provider Router</a> (MPR) calls <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set the Windows error returned from a network provider.
			


## -parameters




### -param err [in]

The error that occurred. This is a network-specific error code.


### -param lpError [in]

String that describes the network-specific error.


### -param lpProviders

TBD




#### - lpProvider [in]

String that names the network provider that raised the error.


## -returns



This function does not return a value.




## -remarks



This function is implemented by the Windows operating system and can be called by network providers.

A provider should use this function to report errors that contain provider-specific information. The error information is saved until it is overwritten by another call to <b>WNetSetLastError</b> in the same thread.

The recommended way for a provider function to handle general errors is to use the following statement.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>return(providerError);
</pre>
</td>
</tr>
</table></span></div>
In this statement, providerError is a Windows error code, such as one of the return codes listed for the provider API in this document.

For provider-specific errors, a provider should do the following.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Set up lpErrorString to be the error to be reported.
WNetSetLastError(providerError,
lpErrorString,
lpProviderName) ;
return(ERROR_EXTENDED_ERROR) ;
</pre>
</td>
</tr>
</table></span></div>
In this case, providerError is the provider-specific error code.

Providers do not need to call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> before returning from a provider function. The MPR calls <b>SetLastError</b> to set the Windows error returned from a provider when necessary to satisfy applications.



