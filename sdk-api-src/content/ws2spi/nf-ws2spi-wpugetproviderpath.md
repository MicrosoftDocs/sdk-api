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

# WPUGetProviderPath function


## -description



			The 
<b>WPUGetProviderPath</b> function retrieves the DLL path for the specified provider.


## -parameters




### -param lpProviderId [in]

Locally unique identifier of the provider. This must be a value obtained by using 
<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>.


### -param lpszProviderDllPath [out]

Pointer to a buffer containing a string that identifies the provider DLL's path. This path is a null-terminated string and any embedded environment strings (such as %SystemRoot%) have not been expanded.


### -param lpProviderDllPathLen [in, out]

Size of the buffer pointed to by <i>lpszProviderDllPath</i>, in characters.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, 
<b>WPUGetProviderPath</b> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
Either <i>lpszProviderDllPath</i> or <i>lpErrno</i> is not in a valid part of the user address space, or <i>lpProviderDllPathLen</i> is too small.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>WPUGetProviderPath</b> function retrieves the DLL path for the specified provider. The DLL path is null-terminated and may contain embedded environment strings (such as %SystemRoot%). Thus, the string should be expanded prior to being used with <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>. For more information, see <b>LoadLibrary</b>.




## -see-also




<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>



<a href="https://msdn.microsoft.com/c0736018-2bcf-4281-aa73-3e1ff9eac92e">WSCInstallProvider</a>
 

 

