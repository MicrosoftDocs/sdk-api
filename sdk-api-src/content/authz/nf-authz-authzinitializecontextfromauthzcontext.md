---
UID: NF:authz.AuthzInitializeContextFromAuthzContext
title: AuthzInitializeContextFromAuthzContext function
author: windows-sdk-content
description: Creates a new client context based on an existing client context.
old-location: security\authzinitializecontextfromauthzcontext.htm
tech.root: secauthz
ms.assetid: dac5e354-ee31-45e3-9eb8-8f3263161ad2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AuthzInitializeContextFromAuthzContext, AuthzInitializeContextFromAuthzContext function [Security], _win32_authzinitializecontextfromauthzcontext, authz/AuthzInitializeContextFromAuthzContext, security.authzinitializecontextfromauthzcontext
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
 - Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
 - AuthzInitializeContextFromAuthzContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# AuthzInitializeContextFromAuthzContext function


## -description


The <b>AuthzInitializeContextFromAuthzContext</b> function creates a new client context based on an existing client context. 

Starting with Windows Server 2012 and Windows 8, this function also duplicates device groups, user claims, and device claims.


## -parameters




### -param Flags [in]

Reserved for future use.


### -param hAuthzClientContext [in]

The handle to an existing client context.


### -param pExpirationTime [in, optional]

Sets the time limit for how long the returned context structure is valid. If no value is passed, then the token never expires. Expiration time is not currently enforced.


### -param Identifier [in]

The specific identifier for the resource manager.


### -param DynamicGroupArgs [in]

A pointer to parameters to be passed to the callback function that computes dynamic groups. If the value is <b>NULL</b>, then the callback function is not called.


### -param phNewAuthzClientContext [out]

A pointer to the duplicated AUTHZ_CLIENT_CONTEXT_HANDLE handle. When you have finished using the handle, release it by calling the <a href="https://msdn.microsoft.com/cad9fff0-9aa6-4cb2-a34f-94cf72f66bca">AuthzFreeContext</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function calls the  <a href="https://msdn.microsoft.com/c20a02a0-5303-4433-a484-5a89999b32b9">AuthzComputeGroupsCallback</a> callback function to add <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> to the newly created context.




## -see-also




<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

