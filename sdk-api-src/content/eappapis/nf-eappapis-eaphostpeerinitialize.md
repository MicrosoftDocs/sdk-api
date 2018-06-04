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

# EapHostPeerInitialize function


## -description


Initializes an EAPHost authentication session. 

The <b>EapHostPeerInitialize</b> function must be called before any other peer or supplicant function is called. If the <b>EapHostPeerInitialize</b> function fails, do not call any other EAPHost run-time API. <div class="alert"><b>Note</b>  The other EAPHost configuration APIs aren't affected by the failure of <b>EAPHostPeerInitialize.</b></div>
<div> </div>



## -parameters






## -remarks



<b>EapHostPeerInitialize</b> and <a href="https://msdn.microsoft.com/5d3a101a-4de3-4da2-8c03-e672e206ffb0">EapHostPeerUninitialize</a> are always thread
safe.

The following call occurs within the <b>EapHostPeerInitialize</b> function:

<code>CoInitializeEx(NULL, COINIT_MULTITHREADED);</code>

The client should not initialize a conflicting COM environment.
If different COM environment (such as a single-threaded apartment) is required, the client should call  <a href="_com_CoInitializeEx">CoInitializeEx</a> directly, and not call <b>EapHostPeerInitialize</b>. If <b>CoInitializeEx</b> is called directly, then the client must call <a href="_com_CoUninitialize">CoUninitialize</a> to uninitialize the session. In addition, the client must use COM functions (and not EAPHost supplicant functions) to allocate and free memory.




## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/5d3a101a-4de3-4da2-8c03-e672e206ffb0">EapHostPeerUninitialize</a>
 

 

