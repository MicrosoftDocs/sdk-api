---
UID: NF:azroles.IAzClientContext.get_UserDn
title: IAzClientContext::get_UserDn (azroles.h)
description: Retrieves the name of the current client in distinguished name (DN) format.
helpviewer_keywords: ["AzClientContext object [Security]","UserDn property","IAzClientContext interface [Security]","UserDn property","IAzClientContext.UserDn","IAzClientContext.get_UserDn","IAzClientContext::UserDn","IAzClientContext::get_UserDn","UserDn property [Security]","UserDn property [Security]","AzClientContext object","UserDn property [Security]","IAzClientContext interface","azroles/IAzClientContext::UserDn","azroles/IAzClientContext::get_UserDn","get_UserDn","security.iazclientcontext_userdn"]
old-location: security\iazclientcontext_userdn.htm
tech.root: security
ms.assetid: 1561352c-254e-41a2-bfc9-795a678ce180
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],UserDn property, IAzClientContext interface [Security],UserDn property, IAzClientContext.UserDn, IAzClientContext.get_UserDn, IAzClientContext::UserDn, IAzClientContext::get_UserDn, UserDn property [Security], UserDn property [Security],AzClientContext object, UserDn property [Security],IAzClientContext interface, azroles/IAzClientContext::UserDn, azroles/IAzClientContext::get_UserDn, get_UserDn, security.iazclientcontext_userdn
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
 - IAzClientContext::get_UserDn
 - azroles/IAzClientContext::get_UserDn
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
 - IAzClientContext.UserDn
 - IAzClientContext.get_UserDn
 - AzClientContext.UserDn
---

# IAzClientContext::get_UserDn


## -description

The <b>UserDn</b> property retrieves the name of the current client in distinguished name (DN) format.

This property is read-only.

## -parameters

## -remarks

The DN client name is retrieved by impersonating the client token and calling the <a href="/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function with <b>NameFullyQualifiedDN</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in DN format is "CN=Ben Smith, OU=Software, OU=Example, O=FourthCoffee, C=US".