---
UID: NF:azroles.IAzClientContext.get_UserDnsSamCompat
title: IAzClientContext::get_UserDnsSamCompat
author: windows-sdk-content
description: Retrieves the name of the current client in a DNS format compatible with Windows&#160;Security&#160;Account&#160;Manager (SAM).
old-location: security\iazclientcontext_userdnssamcompat.htm
old-project: secauthz
ms.assetid: 8f2739cd-3add-4a3c-9c00-8b23d2cec068
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzClientContext object [Security],UserDnsSamCompat property, IAzClientContext interface [Security],UserDnsSamCompat property, IAzClientContext.UserDnsSamCompat, IAzClientContext.get_UserDnsSamCompat, IAzClientContext::UserDnsSamCompat, IAzClientContext::get_UserDnsSamCompat, UserDnsSamCompat property [Security], UserDnsSamCompat property [Security],AzClientContext object, UserDnsSamCompat property [Security],IAzClientContext interface, azroles/IAzClientContext::UserDnsSamCompat, azroles/IAzClientContext::get_UserDnsSamCompat, get_UserDnsSamCompat, security.iazclientcontext_userdnssamcompat
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
 - IAzClientContext.UserDnsSamCompat
 - IAzClientContext.get_UserDnsSamCompat
 - AzClientContext.UserDnsSamCompat
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext::get_UserDnsSamCompat


## -description


The <b>UserDnsSamCompat</b> property retrieves the name of the current client in a DNS format compatible with Windows Security Account Manager (SAM).

This property is read-only.


## -parameters


## -remarks



The SAM-compatible DNS client name is retrieved by impersonating the client token and calling the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function with <b>NameDnsDomain</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in SAM-compatible DNS format is "example.fourthcoffee.com\Username".



