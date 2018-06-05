---
UID: NF:authz.AuthzInitializeContextFromToken
title: AuthzInitializeContextFromToken function
author: windows-sdk-content
description: Initializes a client authorization context from a kernel token. The kernel token must have been opened for TOKEN_QUERY.
old-location: security\authzinitializecontextfromtoken.htm
old-project: SecAuthZ
ms.assetid: 75a7fb3f-6b3a-42ca-b467-f57baf6c60c6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AuthzInitializeContextFromToken, AuthzInitializeContextFromToken function [Security], _win32_authzinitializecontextfromtoken, authz/AuthzInitializeContextFromToken, security.authzinitializecontextfromtoken
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Authz.dll
-	Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
-	AuthzInitializeContextFromToken
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzInitializeContextFromToken function


## -description


The <b>AuthzInitializeContextFromToken</b> function initializes a client authorization context from a kernel token. The kernel token must have been opened for TOKEN_QUERY. 

Starting with Windows Server 2012 and Windows 8, this function can also copy device groups, user claims, and device claims.


## -parameters




### -param Flags [in]

Reserved for future use.


### -param TokenHandle [in]

A handle to the client token used to initialize the <i>pAuthzClientContext</i> parameter. The token must have been opened with TOKEN_QUERY access.


### -param hAuthzResourceManager [in]

A handle to the resource manager that created this client context. This handle is stored in the client context structure.


### -param pExpirationTime [in, optional]

Expiration date and time of the token. If no value is passed, the token never expires. Expiration time is not currently enforced.


### -param Identifier [in]

Identifier that is specific to the resource manager. This parameter is not currently used.


### -param DynamicGroupArgs [in, optional]

A pointer to parameters to be passed to the callback function that computes dynamic groups.


### -param phAuthzClientContext [out]

A pointer to the <i>AuthzClientContext</i> handle returned. Call 
<a href="https://msdn.microsoft.com/cad9fff0-9aa6-4cb2-a34f-94cf72f66bca">AuthzFreeContext</a> when done with the client context.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function calls the  <a href="https://msdn.microsoft.com/c20a02a0-5303-4433-a484-5a89999b32b9">AuthzComputeGroupsCallback</a> callback function to add <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> to the newly created context.




## -see-also




<a href="https://msdn.microsoft.com/cad9fff0-9aa6-4cb2-a34f-94cf72f66bca">AuthzFreeContext</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

