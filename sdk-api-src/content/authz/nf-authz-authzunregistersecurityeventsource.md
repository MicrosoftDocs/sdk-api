---
UID: NF:authz.AuthzUnregisterSecurityEventSource
title: AuthzUnregisterSecurityEventSource function
author: windows-sdk-content
description: Unregisters a security event source with the Local Security Authority (LSA).
old-location: security\authzunregistersecurityeventsource.htm
old-project: secauthz
ms.assetid: 3ca3086b-f9c9-4305-aaf3-c41b5dba30ad
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AuthzUnregisterSecurityEventSource, AuthzUnregisterSecurityEventSource function [Security], authz/AuthzUnregisterSecurityEventSource, security.authzunregistersecurityeventsource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzUnregisterSecurityEventSource
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzUnregisterSecurityEventSource function


## -description


The <b>AuthzUnregisterSecurityEventSource</b> function unregisters a security event source with the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA).


## -parameters




### -param dwFlags [in]

This parameter is reserved for future use. Set this parameter to zero.


### -param phEventProvider [in, out]

A pointer to a handle to the security event source to unregister.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function deallocates any resources and closes any RPC connections associated with a previous call to the <a href="https://msdn.microsoft.com/726e480d-1a34-4fd6-ac2d-876fa08f4eae">AuthzRegisterSecurityEventSource</a> function.




## -see-also




<a href="https://msdn.microsoft.com/726e480d-1a34-4fd6-ac2d-876fa08f4eae">AuthzRegisterSecurityEventSource</a>
 

 

