---
UID: NF:azroles.IAzClientContext.get_UserDisplay
title: IAzClientContext::get_UserDisplay (azroles.h)
description: Retrieves the name of the current client in user display name format.
old-location: security\iazclientcontext_userdisplay.htm
tech.root: SecAuthZ
ms.assetid: db75ecc1-0096-4e14-a5be-10b596ad5163
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],UserDisplay property, IAzClientContext interface [Security],UserDisplay property, IAzClientContext.UserDisplay, IAzClientContext.get_UserDisplay, IAzClientContext::UserDisplay, IAzClientContext::get_UserDisplay, UserDisplay property [Security], UserDisplay property [Security],AzClientContext object, UserDisplay property [Security],IAzClientContext interface, azroles/IAzClientContext::UserDisplay, azroles/IAzClientContext::get_UserDisplay, get_UserDisplay, security.iazclientcontext_userdisplay
f1_keywords:
- azroles/IAzClientContext.UserDisplay
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzClientContext.UserDisplay
- IAzClientContext.get_UserDisplay
- AzClientContext.UserDisplay
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzClientContext::get_UserDisplay


## -description


The <b>UserDisplay</b> property retrieves the name of the current client in user display name format.

This property is read-only.


## -parameters


## -remarks



The user display client name is retrieved by impersonating the client token and calling the <a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function with <b>NameCanonical</b> specified for the <i>NameDisplay</i> parameter. 

An example of a  client name in user display name format is "Ben Smith". 



