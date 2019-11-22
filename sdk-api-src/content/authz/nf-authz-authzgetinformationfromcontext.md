---
UID: NF:authz.AuthzGetInformationFromContext
title: AuthzGetInformationFromContext function (authz.h)

description: Returns information about an Authz context.
old-location: security\authzgetinformationfromcontext.htm
tech.root: SecAuthZ
ms.assetid: c365029a-3ff3-49c1-9dfc-b52948e466f3

ms.date: 12/05/2018
ms.keywords: AuthzGetInformationFromContext, AuthzGetInformationFromContext function [Security], _win32_authzgetinformationfromcontext, authz/AuthzGetInformationFromContext, security.authzgetinformationfromcontext
ms.topic: function
f1_keywords:
- authz/AuthzGetInformationFromContext
dev_langs:
 - c++
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Authz.dll
api_name:
- AuthzGetInformationFromContext
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# AuthzGetInformationFromContext function


## -description


The <b>AuthzGetInformationFromContext</b> function returns information about an Authz context. 

Starting with Windows Server 2012 and Windows 8, device groups are returned as a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure. User and device claims are returned as an <a href="https://docs.microsoft.com/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure.


## -parameters




### -param hAuthzClientContext [in]

A handle to the context.


### -param InfoClass [in]

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/authz/ne-authz-authz_context_information_class">AUTHZ_CONTEXT_INFORMATION_CLASS</a> enumeration that indicates the type of information to be returned.


### -param BufferSize [in]

Size of the buffer passed.


### -param pSizeRequired [out]

A pointer to a <b>DWORD</b> of  the buffer size required for returning the structure.


### -param Buffer [out]

A pointer to memory that can receive the information. The structure returned depends on the information requested in the <i>InfoClass</i> parameter.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/authz/ne-authz-authz_context_information_class">AUTHZ_CONTEXT_INFORMATION_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>
 

 

