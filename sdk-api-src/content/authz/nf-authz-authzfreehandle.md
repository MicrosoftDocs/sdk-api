---
UID: NF:authz.AuthzFreeHandle
title: AuthzFreeHandle function (authz.h)
description: Finds and deletes a handle from the handle list.
helpviewer_keywords: ["AuthzFreeHandle","AuthzFreeHandle function [Security]","_win32_authzfreehandle","authz/AuthzFreeHandle","security.authzfreehandle"]
old-location: security\authzfreehandle.htm
tech.root: security
ms.assetid: 8d2e2ae9-b515-4a02-b366-5b107b4f7ffa
ms.date: 12/05/2018
ms.keywords: AuthzFreeHandle, AuthzFreeHandle function [Security], _win32_authzfreehandle, authz/AuthzFreeHandle, security.authzfreehandle
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - AuthzFreeHandle
 - authz/AuthzFreeHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzFreeHandle
---

# AuthzFreeHandle function


## -description

The <b>AuthzFreeHandle</b> function finds and deletes a handle from the handle list.

## -parameters

### -param hAccessCheckResults [in]

A handle to be freed.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>