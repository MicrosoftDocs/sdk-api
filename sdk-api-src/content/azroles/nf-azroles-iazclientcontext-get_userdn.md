---
UID: NF:azroles.IAzClientContext.get_UserDn
title: IAzClientContext::get_UserDn
author: windows-sdk-content
description: Retrieves the name of the current client in distinguished name (DN) format.
old-location: security\iazclientcontext_userdn.htm
old-project: secauthz
ms.assetid: 1561352c-254e-41a2-bfc9-795a678ce180
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AzClientContext object [Security],UserDn property, IAzClientContext interface [Security],UserDn property, IAzClientContext.UserDn, IAzClientContext.get_UserDn, IAzClientContext::UserDn, IAzClientContext::get_UserDn, UserDn property [Security], UserDn property [Security],AzClientContext object, UserDn property [Security],IAzClientContext interface, azroles/IAzClientContext::UserDn, azroles/IAzClientContext::get_UserDn, get_UserDn, security.iazclientcontext_userdn
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
 - IAzClientContext.UserDn
 - IAzClientContext.get_UserDn
 - AzClientContext.UserDn
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext::get_UserDn


## -description


The <b>UserDn</b> property retrieves the name of the current client in distinguished name (DN) format.

This property is read-only.


## -parameters


## -remarks



The DN client name is retrieved by impersonating the client token and calling the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function with <b>NameFullyQualifiedDN</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in DN format is "CN=Ben Smith, OU=Software, OU=Example, O=FourthCoffee, C=US". 



