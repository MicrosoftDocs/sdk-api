---
UID: NF:authz.AuthzGetInformationFromContext
title: AuthzGetInformationFromContext function
author: windows-sdk-content
description: Returns information about an Authz context.
old-location: security\authzgetinformationfromcontext.htm
tech.root: secauthz
ms.assetid: c365029a-3ff3-49c1-9dfc-b52948e466f3
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AuthzGetInformationFromContext, AuthzGetInformationFromContext function [Security], _win32_authzgetinformationfromcontext, authz/AuthzGetInformationFromContext, security.authzgetinformationfromcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- 
: 
- AuthzGetInformationFromContext
: 
---

# AuthzGetInformationFromContext function


## -description


The <b>AuthzGetInformationFromContext</b> function returns information about an Authz context. 

Starting with Windows Server 2012 and Windows 8, device groups are returned as a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure. User and device claims are returned as an <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure.


## -parameters




### -param hAuthzClientContext [in]

A handle to the context.


### -param InfoClass [in]

A value of the <a href="https://msdn.microsoft.com/5eb752dc-17f7-4510-8aef-d18280322e76">AUTHZ_CONTEXT_INFORMATION_CLASS</a> enumeration that indicates the type of information to be returned.


### -param BufferSize [in]

Size of the buffer passed.


### -param pSizeRequired [out]

A pointer to a <b>DWORD</b> of  the buffer size required for returning the structure.


### -param Buffer [out]

A pointer to memory that can receive the information. The structure returned depends on the information requested in the <i>InfoClass</i> parameter.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/5eb752dc-17f7-4510-8aef-d18280322e76">AUTHZ_CONTEXT_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>
 

 

