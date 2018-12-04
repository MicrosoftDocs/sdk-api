---
UID: NF:azroles.IAzApplicationGroup.get_AppMembers
title: IAzApplicationGroup::get_AppMembers
author: windows-sdk-content
description: Retrieves the application groups that belong to this application group.
old-location: security\iazapplicationgroup_appmembers.htm
tech.root: secauthz
ms.assetid: 74239ac2-b6ea-4839-b4c5-7a77d454aa0b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: AppMembers property [Security], AppMembers property [Security],AzApplicationGroup object, AppMembers property [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AppMembers property, IAzApplicationGroup interface [Security],AppMembers property, IAzApplicationGroup.AppMembers, IAzApplicationGroup.get_AppMembers, IAzApplicationGroup::AppMembers, IAzApplicationGroup::get_AppMembers, azroles/IAzApplicationGroup::AppMembers, azroles/IAzApplicationGroup::get_AppMembers, get_AppMembers, security.iazapplicationgroup_appmembers
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
 - IAzApplicationGroup.AppMembers
 - IAzApplicationGroup.get_AppMembers
 - AzApplicationGroup.AppMembers
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::get_AppMembers


## -description


The <b>AppMembers</b> property retrieves the application groups that belong to this application group.

This property is read-only.


## -parameters


## -remarks



This property allows the nesting of <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects within another <b>IAzApplicationGroup</b> object.

In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



