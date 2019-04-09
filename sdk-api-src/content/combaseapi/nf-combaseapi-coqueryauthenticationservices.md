---
UID: NF:combaseapi.CoQueryAuthenticationServices
title: CoQueryAuthenticationServices function (combaseapi.h)
author: windows-sdk-content
description: Retrieves a list of the authentication services registered when the process called CoInitializeSecurity.
old-location: com\coqueryauthenticationservices.htm
tech.root: com
ms.assetid: e9e7c5a3-70ec-4a68-ac21-1ab6774d140f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoQueryAuthenticationServices, CoQueryAuthenticationServices function [COM], _com_CoQueryAuthenticationServices, com.coqueryauthenticationservices, combaseapi/CoQueryAuthenticationServices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoQueryAuthenticationServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoQueryAuthenticationServices function


## -description


Retrieves a list of the authentication services registered when the process called <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>.


## -parameters




### -param pcAuthSvc [out]

A pointer to a variable that receives the number of entries returned in the <i>asAuthSvc</i> array.


### -param asAuthSvc [out]

A pointer to an array of <a href="https://msdn.microsoft.com/77fd15d7-54d4-4812-93d3-13a671e7afff">SOLE_AUTHENTICATION_SERVICE</a> structures. The list is allocated through a call to the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function. The caller must free the list when finished with it by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.



## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



<b>CoQueryAuthenticationServices</b> retrieves a list of the authentication services currently registered. If the process calls <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>, these are the services registered through that call. If the application does not call it, <b>CoInitializeSecurity</b> is called automatically by COM, registering the default security package, the first time an interface is marshaled or unmarshaled. 

This function returns only the authentication services registered with <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>. It does not return all of the authentication services installed on the computer, but <a href="https://msdn.microsoft.com/900790a6-111d-43f5-9316-e85aab03a3bc">EnumerateSecurityPackages</a> does. <b>CoQueryAuthenticationServices</b> is primarily useful for custom marshalers, to determine which principal names an application can use.

Different authentication services support different levels of security. For example, NTLMSSP does not support delegation or mutual authentication while Kerberos does. The application is responsible only for registering authentication services that provide the features the application needs. This function provides a way to find out which services have been registered with <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>.





## -see-also




<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>



<a href="https://msdn.microsoft.com/77fd15d7-54d4-4812-93d3-13a671e7afff">SOLE_AUTHENTICATION_SERVICE</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

