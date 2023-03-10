---
UID: NF:azroles.IAzClientContext.get_UserUpn
title: IAzClientContext::get_UserUpn (azroles.h)
description: Retrieves the name of the current client in user principal name (UPN) format.
helpviewer_keywords: ["AzClientContext object [Security]","UserUpn property","IAzClientContext interface [Security]","UserUpn property","IAzClientContext.UserUpn","IAzClientContext.get_UserUpn","IAzClientContext::UserUpn","IAzClientContext::get_UserUpn","UserUpn property [Security]","UserUpn property [Security]","AzClientContext object","UserUpn property [Security]","IAzClientContext interface","azroles/IAzClientContext::UserUpn","azroles/IAzClientContext::get_UserUpn","get_UserUpn","security.iazclientcontext_userupn"]
old-location: security\iazclientcontext_userupn.htm
tech.root: security
ms.assetid: e54d450b-7059-43c7-9c08-688975031401
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],UserUpn property, IAzClientContext interface [Security],UserUpn property, IAzClientContext.UserUpn, IAzClientContext.get_UserUpn, IAzClientContext::UserUpn, IAzClientContext::get_UserUpn, UserUpn property [Security], UserUpn property [Security],AzClientContext object, UserUpn property [Security],IAzClientContext interface, azroles/IAzClientContext::UserUpn, azroles/IAzClientContext::get_UserUpn, get_UserUpn, security.iazclientcontext_userupn
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
 - IAzClientContext::get_UserUpn
 - azroles/IAzClientContext::get_UserUpn
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
 - IAzClientContext.UserUpn
 - IAzClientContext.get_UserUpn
 - AzClientContext.UserUpn
---

# IAzClientContext::get_UserUpn


## -description

The <b>UserUpn</b> property retrieves the name of the current client in user principal name (UPN) format.

This property is read-only.

## -parameters

## -remarks

The UPN client name is retrieved by impersonating the client token and calling the <a href="/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function with <b>NameUserPrincipal</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in UPN format is "someone@example.com".