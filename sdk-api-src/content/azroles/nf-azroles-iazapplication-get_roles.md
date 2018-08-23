---
UID: NF:azroles.IAzApplication.get_Roles
title: IAzApplication::get_Roles
author: windows-sdk-content
description: The Roles property of IAzApplication retrieves an IAzRoles object that is used to enumerate IAzRole objects from the policy data.
old-location: security\iazapplication_roles.htm
old-project: secauthz
ms.assetid: 02acf473-b072-4814-92e1-47a32baae4fc
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzApplication object [Security],Roles property, IAzApplication interface [Security],Roles property, IAzApplication.Roles, IAzApplication.get_Roles, IAzApplication::Roles, IAzApplication::get_Roles, Roles property [Security], Roles property [Security],AzApplication object, Roles property [Security],IAzApplication interface, azroles/IAzApplication::Roles, azroles/IAzApplication::get_Roles, get_Roles, security.iazapplication_roles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
 - IAzApplication.Roles
 - IAzApplication.get_Roles
 - AzApplication.Roles
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::get_Roles


## -description


The <b>Roles</b> property retrieves an <a href="https://msdn.microsoft.com/bc69ec52-ea73-4a0c-a9a2-913a6725489e">IAzRoles</a> object that is used to enumerate <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



