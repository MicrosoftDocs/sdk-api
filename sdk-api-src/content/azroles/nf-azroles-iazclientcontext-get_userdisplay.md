---
UID: NF:azroles.IAzClientContext.get_UserDisplay
title: IAzClientContext::get_UserDisplay
author: windows-driver-content
description: Retrieves the name of the current client in user display name format.
old-location: security\iazclientcontext_userdisplay.htm
old-project: SecAuthZ
ms.assetid: db75ecc1-0096-4e14-a5be-10b596ad5163
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzClientContext object [Security],UserDisplay property, IAzClientContext interface [Security],UserDisplay property, IAzClientContext.UserDisplay, IAzClientContext.get_UserDisplay, IAzClientContext::UserDisplay, IAzClientContext::get_UserDisplay, UserDisplay property [Security], UserDisplay property [Security],AzClientContext object, UserDisplay property [Security],IAzClientContext interface, azroles/IAzClientContext::UserDisplay, azroles/IAzClientContext::get_UserDisplay, get_UserDisplay, security.iazclientcontext_userdisplay
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzClientContext.UserDisplay
-	IAzClientContext.get_UserDisplay
-	AzClientContext.UserDisplay
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext::get_UserDisplay


## -description


The <b>UserDisplay</b> property retrieves the name of the current client in user display name format.

This property is read-only.


## -parameters


## -remarks



The user display client name is retrieved by impersonating the client token and calling the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function with <b>NameCanonical</b> specified for the <i>NameDisplay</i> parameter. 

An example of a  client name in user display name format is "Ben Smith". 



