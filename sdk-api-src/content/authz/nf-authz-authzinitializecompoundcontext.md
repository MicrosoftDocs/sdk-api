---
UID: NF:authz.AuthzInitializeCompoundContext
title: AuthzInitializeCompoundContext function (authz.h)
author: windows-sdk-content
description: Creates a user-mode context from the given user and device security contexts.
old-location: security\authzinitializecompoundcontext.htm
tech.root: SecAuthZ
ms.assetid: 2EC9EE76-9A92-40DF-9884-547D96FF3E09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AuthzInitializeCompoundContext, AuthzInitializeCompoundContext function [Security], authz/AuthzInitializeCompoundContext, security.authzinitializecompoundcontext
ms.topic: function
f1_keywords: 
 - "authz/AuthzInitializeCompoundContext"
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - AuthzInitializeCompoundContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuthzInitializeCompoundContext function


## -description


The <b>AuthzInitializeCompoundContext</b> function creates a user-mode context from the given user and device security contexts.


## -parameters




### -param UserContext [in]

User context to create the compound context from.


### -param DeviceContext [in]

Device context to create the compound context from. This must not be the same as the user context.


### -param phCompoundContext [out]

Used to return the resultant compound context.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



