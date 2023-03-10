---
UID: NF:azroles.IAzClientContext.get_RoleForAccessCheck
title: IAzClientContext::get_RoleForAccessCheck (azroles.h)
description: Sets or retrieves the role that is used to perform the access check. (Get)
helpviewer_keywords: ["AzClientContext object [Security]","RoleForAccessCheck property","IAzClientContext interface [Security]","RoleForAccessCheck property","IAzClientContext.RoleForAccessCheck","IAzClientContext.get_RoleForAccessCheck","IAzClientContext::RoleForAccessCheck","IAzClientContext::get_RoleForAccessCheck","IAzClientContext::put_RoleForAccessCheck","RoleForAccessCheck property [Security]","RoleForAccessCheck property [Security]","AzClientContext object","RoleForAccessCheck property [Security]","IAzClientContext interface","azroles/IAzClientContext::RoleForAccessCheck","azroles/IAzClientContext::get_RoleForAccessCheck","azroles/IAzClientContext::put_RoleForAccessCheck","get_RoleForAccessCheck","security.iazclientcontext_roleforaccesscheck"]
old-location: security\iazclientcontext_roleforaccesscheck.htm
tech.root: security
ms.assetid: 817b3693-b989-431c-a8b3-bdeeb0367dc6
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],RoleForAccessCheck property, IAzClientContext interface [Security],RoleForAccessCheck property, IAzClientContext.RoleForAccessCheck, IAzClientContext.get_RoleForAccessCheck, IAzClientContext::RoleForAccessCheck, IAzClientContext::get_RoleForAccessCheck, IAzClientContext::put_RoleForAccessCheck, RoleForAccessCheck property [Security], RoleForAccessCheck property [Security],AzClientContext object, RoleForAccessCheck property [Security],IAzClientContext interface, azroles/IAzClientContext::RoleForAccessCheck, azroles/IAzClientContext::get_RoleForAccessCheck, azroles/IAzClientContext::put_RoleForAccessCheck, get_RoleForAccessCheck, security.iazclientcontext_roleforaccesscheck
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzClientContext::get_RoleForAccessCheck
 - azroles/IAzClientContext::get_RoleForAccessCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext.RoleForAccessCheck
 - IAzClientContext.get_RoleForAccessCheck
 - IAzClientContext.put_RoleForAccessCheck
 - AzClientContext.RoleForAccessCheck
---

# IAzClientContext::get_RoleForAccessCheck


## -description

The <b>RoleForAccessCheck</b> property sets or retrieves the role that is used to perform the access check.

This property is read/write.

## -parameters

## -remarks

If this property is set, the role specified by this property will be the only role used in the access check; otherwise, all roles contained in the context will be used.

