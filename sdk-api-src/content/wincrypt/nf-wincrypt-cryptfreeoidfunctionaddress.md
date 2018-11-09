---
UID: NF:wincrypt.CryptFreeOIDFunctionAddress
title: CryptFreeOIDFunctionAddress function
author: windows-sdk-content
description: The CryptFreeOIDFunctionAddress function releases a handle returned by CryptGetOIDFunctionAddress or CryptGetDefaultOIDFunctionAddress by decrementing the reference count on the function handle.
old-location: security\cryptfreeoidfunctionaddress.htm
tech.root: seccrypto
ms.assetid: cacacff3-25b7-4ed4-885b-b4b0b326628f
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CryptFreeOIDFunctionAddress, CryptFreeOIDFunctionAddress function [Security], _crypto2_cryptfreeoidfunctionaddress, security.cryptfreeoidfunctionaddress, wincrypt/CryptFreeOIDFunctionAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptFreeOIDFunctionAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

