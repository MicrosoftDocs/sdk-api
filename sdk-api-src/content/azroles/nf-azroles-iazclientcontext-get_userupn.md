---
UID: NF:azroles.IAzClientContext.get_UserUpn
title: IAzClientContext::get_UserUpn
author: windows-sdk-content
description: Retrieves the name of the current client in user principal name (UPN) format.
old-location: security\iazclientcontext_userupn.htm
old-project: secauthz
ms.assetid: e54d450b-7059-43c7-9c08-688975031401
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzClientContext object [Security],UserUpn property, IAzClientContext interface [Security],UserUpn property, IAzClientContext.UserUpn, IAzClientContext.get_UserUpn, IAzClientContext::UserUpn, IAzClientContext::get_UserUpn, UserUpn property [Security], UserUpn property [Security],AzClientContext object, UserUpn property [Security],IAzClientContext interface, azroles/IAzClientContext::UserUpn, azroles/IAzClientContext::get_UserUpn, get_UserUpn, security.iazclientcontext_userupn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext::get_UserUpn


## -description


The <b>UserUpn</b> property retrieves the name of the current client in user principal name (UPN) format.

This property is read-only.


## -parameters


## -remarks



The UPN client name is retrieved by impersonating the client token and calling the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function with <b>NameUserPrincipal</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in UPN format is "someone@example.com". 



