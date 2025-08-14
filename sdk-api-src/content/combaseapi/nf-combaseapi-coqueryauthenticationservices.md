---
UID: NF:combaseapi.CoQueryAuthenticationServices
title: CoQueryAuthenticationServices function (combaseapi.h)
description: Retrieves a list of the authentication services registered when the process called CoInitializeSecurity.
helpviewer_keywords: ["CoQueryAuthenticationServices","CoQueryAuthenticationServices function [COM]","_com_CoQueryAuthenticationServices","com.coqueryauthenticationservices","combaseapi/CoQueryAuthenticationServices"]
old-location: com\coqueryauthenticationservices.htm
tech.root: com
ms.assetid: e9e7c5a3-70ec-4a68-ac21-1ab6774d140f
ms.date: 12/05/2018
ms.keywords: CoQueryAuthenticationServices, CoQueryAuthenticationServices function [COM], _com_CoQueryAuthenticationServices, com.coqueryauthenticationservices, combaseapi/CoQueryAuthenticationServices
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoQueryAuthenticationServices
 - combaseapi/CoQueryAuthenticationServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoQueryAuthenticationServices
---

# CoQueryAuthenticationServices function


## -description

Retrieves a list of the authentication services registered when the process called <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>.

## -parameters

### -param pcAuthSvc [out]

A pointer to a variable that receives the number of entries returned in the <i>asAuthSvc</i> array.

### -param asAuthSvc [out]

A pointer to an array of <a href="/windows/desktop/api/objidl/ns-objidl-sole_authentication_service">SOLE_AUTHENTICATION_SERVICE</a> structures. The list is allocated through a call to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function. The caller must free the list when finished with it by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

<b>CoQueryAuthenticationServices</b> retrieves a list of the authentication services currently registered. If the process calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>, these are the services registered through that call. If the application does not call it, <b>CoInitializeSecurity</b> is called automatically by COM, registering the default security package, the first time an interface is marshaled or unmarshaled. 

This function returns only the authentication services registered with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>. It does not return all of the authentication services installed on the computer, but <a href="/windows/desktop/api/sspi/nf-sspi-enumeratesecuritypackagesa">EnumerateSecurityPackages</a> does. <b>CoQueryAuthenticationServices</b> is primarily useful for custom marshalers, to determine which principal names an application can use.

Different authentication services support different levels of security. For example, NTLMSSP does not support delegation or mutual authentication while Kerberos does. The application is responsible only for registering authentication services that provide the features the application needs. This function provides a way to find out which services have been registered with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>



<a href="/windows/desktop/api/objidl/ns-objidl-sole_authentication_service">SOLE_AUTHENTICATION_SERVICE</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>