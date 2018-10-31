---
UID: NF:azroles.IAzClientContext.get_UserSamCompat
title: IAzClientContext::get_UserSamCompat
author: windows-sdk-content
description: Retrieves the name of the current client in a format compatible with Windows&#160;Security&#160;Account&#160;Manager (SAM).
old-location: security\iazclientcontext_usersamcompat.htm
tech.root: secauthz
ms.assetid: 3b1f9e8a-cc3b-4be6-b2d9-8e8b3164d46a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AzClientContext object [Security],UserSamCompat property, IAzClientContext interface [Security],UserSamCompat property, IAzClientContext.UserSamCompat, IAzClientContext.get_UserSamCompat, IAzClientContext::UserSamCompat, IAzClientContext::get_UserSamCompat, UserSamCompat property [Security], UserSamCompat property [Security],AzClientContext object, UserSamCompat property [Security],IAzClientContext interface, azroles/IAzClientContext::UserSamCompat, azroles/IAzClientContext::get_UserSamCompat, get_UserSamCompat, security.iazclientcontext_usersamcompat
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAzClientContext.UserSamCompat
 - IAzClientContext.get_UserSamCompat
 - AzClientContext.UserSamCompat
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzClientContext::get_UserSamCompat


## -description


The <b>UserSamCompat</b> property retrieves the name of the current client in a format compatible with Windows Security Account Manager (SAM).

This property is read-only.


## -parameters


## -remarks



The SAM-compatible client name is retrieved by impersonating the client token and calling the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function with <b>NameSamCompatible</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in SAM-compatible format is "ExampleDomain\UserName". 



