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

# CryptFreeOIDFunctionAddress function


## -description


The <b>CryptFreeOIDFunctionAddress</b> function releases a handle returned by 
<a href="https://msdn.microsoft.com/2eef6109-a840-48c6-936c-ec0875039c39">CryptGetOIDFunctionAddress</a> or 
<a href="https://msdn.microsoft.com/3977368c-ad13-43f9-859b-10c7f170f482">CryptGetDefaultOIDFunctionAddress</a> by decrementing the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on the function handle. In some cases, the DLL file associated with the function is unloaded. For details, see Remarks.


## -parameters




### -param hFuncAddr [in]

Handle of the function previously obtained from a call to 
<a href="https://msdn.microsoft.com/2eef6109-a840-48c6-936c-ec0875039c39">CryptGetOIDFunctionAddress</a> or 
<a href="https://msdn.microsoft.com/3977368c-ad13-43f9-859b-10c7f170f482">CryptGetDefaultOIDFunctionAddress</a>.


### -param dwFlags [in]

Reserved for future use and must be zero.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -remarks



If the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> becomes zero and a DLL is loaded for the function being freed, the DLL might be unloaded. If the DLL exports the <a href="_com_dllcanunloadnow">DLLCanUnloadNow</a> function, that function is called and its return is checked. An S_FALSE return from this function cancels the unloading of the DLL at this time. If the function returns S_TRUE or if the DLL does not export the <b>DLLCanUnloadNow</b> function, an unloading process is started. In this case, actual unloading is deferred for 15 seconds. If another <b>CryptFreeOIDFunctionAddress</b> or <a href="https://msdn.microsoft.com/3977368c-ad13-43f9-859b-10c7f170f482">CryptGetDefaultOIDFunctionAddress</a> that requires the DLL occurs before the 15 seconds elapse, the deferred unload process is canceled.




## -see-also




<a href="https://msdn.microsoft.com/3977368c-ad13-43f9-859b-10c7f170f482">CryptGetDefaultOIDFunctionAddress</a>



<a href="https://msdn.microsoft.com/2eef6109-a840-48c6-936c-ec0875039c39">CryptGetOIDFunctionAddress</a>



<a href="_com_dllcanunloadnow">DLLCanUnloadNow</a>



<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

