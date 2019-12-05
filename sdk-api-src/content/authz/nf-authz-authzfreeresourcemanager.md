---
UID: NF:authz.AuthzFreeResourceManager
title: AuthzFreeResourceManager function (authz.h)
description: Frees a resource manager object.
old-location: security\authzfreeresourcemanager.htm
tech.root: SecAuthZ
ms.assetid: 8b716368-8d81-4c62-9086-0976b39bbcf8
ms.date: 12/05/2018
ms.keywords: AuthzFreeResourceManager, AuthzFreeResourceManager function [Security], _win32_authzfreeresourcemanager, authz/AuthzFreeResourceManager, security.authzfreeresourcemanager
ms.topic: function
f1_keywords:
- authz/AuthzFreeResourceManager
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
- Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
- AuthzFreeResourceManager
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# AuthzFreeResourceManager function


## -description


The <b>AuthzFreeResourceManager</b> function frees a resource manager object.


## -parameters




### -param hAuthzResourceManager [in]

The <b>AUTHZ_RESOURCE_MANAGER_HANDLE</b> to be freed.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>
 

 

