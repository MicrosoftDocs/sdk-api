---
UID: NF:azroles.IAzClientContext.get_UserDnsSamCompat
title: IAzClientContext::get_UserDnsSamCompat (azroles.h)
description: Retrieves the name of the current client in a DNS format compatible with Windows Security Account Manager (SAM).
helpviewer_keywords: ["AzClientContext object [Security]","UserDnsSamCompat property","IAzClientContext interface [Security]","UserDnsSamCompat property","IAzClientContext.UserDnsSamCompat","IAzClientContext.get_UserDnsSamCompat","IAzClientContext::UserDnsSamCompat","IAzClientContext::get_UserDnsSamCompat","UserDnsSamCompat property [Security]","UserDnsSamCompat property [Security]","AzClientContext object","UserDnsSamCompat property [Security]","IAzClientContext interface","azroles/IAzClientContext::UserDnsSamCompat","azroles/IAzClientContext::get_UserDnsSamCompat","get_UserDnsSamCompat","security.iazclientcontext_userdnssamcompat"]
old-location: security\iazclientcontext_userdnssamcompat.htm
tech.root: security
ms.assetid: 8f2739cd-3add-4a3c-9c00-8b23d2cec068
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],UserDnsSamCompat property, IAzClientContext interface [Security],UserDnsSamCompat property, IAzClientContext.UserDnsSamCompat, IAzClientContext.get_UserDnsSamCompat, IAzClientContext::UserDnsSamCompat, IAzClientContext::get_UserDnsSamCompat, UserDnsSamCompat property [Security], UserDnsSamCompat property [Security],AzClientContext object, UserDnsSamCompat property [Security],IAzClientContext interface, azroles/IAzClientContext::UserDnsSamCompat, azroles/IAzClientContext::get_UserDnsSamCompat, get_UserDnsSamCompat, security.iazclientcontext_userdnssamcompat
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
 - IAzClientContext::get_UserDnsSamCompat
 - azroles/IAzClientContext::get_UserDnsSamCompat
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
 - IAzClientContext.UserDnsSamCompat
 - IAzClientContext.get_UserDnsSamCompat
 - AzClientContext.UserDnsSamCompat
---

# IAzClientContext::get_UserDnsSamCompat


## -description

The <b>UserDnsSamCompat</b> property retrieves the name of the current client in a DNS format compatible with Windows Security Account Manager (SAM).

This property is read-only.

## -parameters

## -remarks

The SAM-compatible DNS client name is retrieved by impersonating the client token and calling the <a href="/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function with <b>NameDnsDomain</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in SAM-compatible DNS format is "example.fourthcoffee.com\Username".