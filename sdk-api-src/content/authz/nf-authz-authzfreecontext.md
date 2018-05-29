---
UID: NF:authz.AuthzFreeContext
title: AuthzFreeContext function
author: windows-sdk-content
description: Frees all structures and memory associated with the client context. The list of handles for a client is freed in this call.
old-location: security\authzfreecontext.htm
old-project: SecAuthZ
ms.assetid: cad9fff0-9aa6-4cb2-a34f-94cf72f66bca
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AuthzFreeContext, AuthzFreeContext function [Security], _win32_authzfreecontext, authz/AuthzFreeContext, security.authzfreecontext
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
-	AuthzFreeContext
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzFreeContext function


## -description


The <b>AuthzFreeContext</b> function frees all structures and memory associated with the client context. The list of handles for a client is freed in this call.

Starting with Windows Server 2012 and Windows 8, this function also frees the memory associated with device groups, user claims, and device claims.


## -parameters




### -param hAuthzClientContext

TBD




#### - AuthzClientContext [in]

The <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure to be freed.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

