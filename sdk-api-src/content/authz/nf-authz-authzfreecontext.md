---
UID: NF:authz.AuthzFreeContext
title: AuthzFreeContext function
author: windows-sdk-content
description: Frees all structures and memory associated with the client context. The list of handles for a client is freed in this call.
old-location: security\authzfreecontext.htm
tech.root: SecAuthZ
ms.assetid: cad9fff0-9aa6-4cb2-a34f-94cf72f66bca
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AuthzFreeContext, AuthzFreeContext function [Security], _win32_authzfreecontext, authz/AuthzFreeContext, security.authzfreecontext
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
 - AuthzFreeContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# AuthzFreeContext function


## -description


The <b>AuthzFreeContext</b> function frees all structures and memory associated with the client context. The list of handles for a client is freed in this call.

Starting with Windows Server 2012 and Windows 8, this function also frees the memory associated with device groups, user claims, and device claims.


## -parameters




### -param hAuthzClientContext [in]

The <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure to be freed.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>
 

 

