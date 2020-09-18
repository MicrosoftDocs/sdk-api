---
UID: NF:azroles.IAzClientContext.get_UserCanonical
title: IAzClientContext::get_UserCanonical (azroles.h)
description: Retrieves the name of the current client in canonical format.
helpviewer_keywords: ["AzClientContext object [Security]","UserCanonical property","IAzClientContext interface [Security]","UserCanonical property","IAzClientContext.UserCanonical","IAzClientContext.get_UserCanonical","IAzClientContext::UserCanonical","IAzClientContext::get_UserCanonical","UserCanonical property [Security]","UserCanonical property [Security]","AzClientContext object","UserCanonical property [Security]","IAzClientContext interface","azroles/IAzClientContext::UserCanonical","azroles/IAzClientContext::get_UserCanonical","get_UserCanonical","security.iazclientcontext_usercanonical"]
old-location: security\iazclientcontext_usercanonical.htm
tech.root: security
ms.assetid: 413cdbbd-a9c6-4117-9df5-d7eb202191a4
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],UserCanonical property, IAzClientContext interface [Security],UserCanonical property, IAzClientContext.UserCanonical, IAzClientContext.get_UserCanonical, IAzClientContext::UserCanonical, IAzClientContext::get_UserCanonical, UserCanonical property [Security], UserCanonical property [Security],AzClientContext object, UserCanonical property [Security],IAzClientContext interface, azroles/IAzClientContext::UserCanonical, azroles/IAzClientContext::get_UserCanonical, get_UserCanonical, security.iazclientcontext_usercanonical
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
 - IAzClientContext::get_UserCanonical
 - azroles/IAzClientContext::get_UserCanonical
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
 - IAzClientContext.UserCanonical
 - IAzClientContext.get_UserCanonical
 - AzClientContext.UserCanonical
---

# IAzClientContext::get_UserCanonical


## -description

The <b>UserCanonical</b> property retrieves the name of the current client in canonical format.

This property is read-only.

## -parameters

## -remarks

The canonical client name is retrieved by impersonating the client token and calling the <a href="/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function with <b>NameCanonical</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in canonical format is "example.fourthcoffee.com/software/Ben Smith".