---
UID: NF:authz.AuthzFreeResourceManager
title: AuthzFreeResourceManager function
author: windows-sdk-content
description: Frees a resource manager object.
old-location: security\authzfreeresourcemanager.htm
old-project: SecAuthZ
ms.assetid: 8b716368-8d81-4c62-9086-0976b39bbcf8
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: AuthzFreeResourceManager, AuthzFreeResourceManager function [Security], _win32_authzfreeresourcemanager, authz/AuthzFreeResourceManager, security.authzfreeresourcemanager
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
 - Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
 - AuthzFreeResourceManager
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzFreeResourceManager function


## -description


The <b>AuthzFreeResourceManager</b> function frees a resource manager object.


## -parameters




### -param hAuthzResourceManager

TBD




#### - AuthzResourceManager [in]

The <b>AUTHZ_RESOURCE_MANAGER_HANDLE</b> to be freed.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa373557(v=VS.85).aspx">Basic Access Control Functions</a>
 

 

