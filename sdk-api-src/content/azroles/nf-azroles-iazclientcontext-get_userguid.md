---
UID: NF:azroles.IAzClientContext.get_UserGuid
title: IAzClientContext::get_UserGuid (azroles.h)
description: Retrieves the name of the current client in GUID format.
helpviewer_keywords: ["AzClientContext object [Security]","UserGuid property","IAzClientContext interface [Security]","UserGuid property","IAzClientContext.UserGuid","IAzClientContext.get_UserGuid","IAzClientContext::UserGuid","IAzClientContext::get_UserGuid","UserGuid property [Security]","UserGuid property [Security]","AzClientContext object","UserGuid property [Security]","IAzClientContext interface","azroles/IAzClientContext::UserGuid","azroles/IAzClientContext::get_UserGuid","get_UserGuid","security.iazclientcontext_userguid"]
old-location: security\iazclientcontext_userguid.htm
tech.root: security
ms.assetid: fd60d1d0-67b9-457f-a01e-6ea470d9db6a
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],UserGuid property, IAzClientContext interface [Security],UserGuid property, IAzClientContext.UserGuid, IAzClientContext.get_UserGuid, IAzClientContext::UserGuid, IAzClientContext::get_UserGuid, UserGuid property [Security], UserGuid property [Security],AzClientContext object, UserGuid property [Security],IAzClientContext interface, azroles/IAzClientContext::UserGuid, azroles/IAzClientContext::get_UserGuid, get_UserGuid, security.iazclientcontext_userguid
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
 - IAzClientContext::get_UserGuid
 - azroles/IAzClientContext::get_UserGuid
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
 - IAzClientContext.UserGuid
 - IAzClientContext.get_UserGuid
 - AzClientContext.UserGuid
---

# IAzClientContext::get_UserGuid


## -description

The <b>UserGuid</b> property retrieves the name of the current client in GUID format.

This property is read-only.

## -parameters

## -remarks

The GUID client name is retrieved by impersonating the client token and calling the <a href="/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function with <b>NameUniqueId</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in GUID format is "{4fa050f0-f561-11cf-bdd9-00aa003a77b6}Ben Smith".