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

# EapHostPeerGetUIContext function


## -description


Obtains the user interface context for the supplicant from EAPHost if the UI is to be raised.

<b>EAPHostPeerGetUIContext</b> is always followed by the following functions.<ul>
<li>
<a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>, and</li>
<li>
<a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a>
</li>
</ul>



## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param pdwSizeOfUIContextData [out]

A pointer to a value that specifies the size, in bytes, of the UI context data  buffer returned in <i>ppUIContextData</i>.


### -param ppUIContextData [out]

A pointer to a pointer to a  buffer that contains the supplicant UI context data from EAPHost. The address pointed to by this parameter is passed to <a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a> as IN parameter <i>pUIContextData</i>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>



<a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a>
 

 

