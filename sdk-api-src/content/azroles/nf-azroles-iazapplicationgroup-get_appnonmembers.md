---
UID: NF:azroles.IAzApplicationGroup.get_AppNonMembers
title: IAzApplicationGroup::get_AppNonMembers method
author: windows-driver-content
description: Retrieves the application groups that are refused membership in this application group.
old-location: security\iazapplicationgroup_appnonmembers.htm
old-project: SecAuthZ
ms.assetid: a85a9004-f3f5-44ce-a0d7-fa450af74917
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AppNonMembers property [Security], AppNonMembers property [Security], AzApplicationGroup object, AppNonMembers property [Security], IAzApplicationGroup interface, AzApplicationGroup object [Security], AppNonMembers property, IAzApplicationGroup, IAzApplicationGroup interface [Security], AppNonMembers property, IAzApplicationGroup.AppNonMembers, IAzApplicationGroup::get_AppNonMembers, azroles/IAzApplicationGroup::AppNonMembers, azroles/IAzApplicationGroup::get_AppNonMembers, get_AppNonMembers,IAzApplicationGroup.get_AppNonMembers, security.iazapplicationgroup_appnonmembers
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
-	IAzApplicationGroup.AppNonMembers
-	IAzApplicationGroup.get_AppNonMembers
-	AzApplicationGroup.AppNonMembers
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::get_AppNonMembers method


## -description


The <b>AppNonMembers</b> property retrieves the application groups that are refused membership in this application group.

This property is read-only.


## -parameters


## -remarks



Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



