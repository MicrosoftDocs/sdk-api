---
UID: NF:azroles.IAzApplicationGroup.get_Members
title: IAzApplicationGroup::get_Members
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs), in text form, of accounts that belong to the application group.
old-location: security\iazapplicationgroup_members.htm
old-project: secauthz
ms.assetid: 1370fe81-a729-477e-a500-1823abb713e1
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzApplicationGroup object [Security],Members property, IAzApplicationGroup interface [Security],Members property, IAzApplicationGroup.Members, IAzApplicationGroup.get_Members, IAzApplicationGroup::Members, IAzApplicationGroup::get_Members, Members property [Security], Members property [Security],AzApplicationGroup object, Members property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::Members, azroles/IAzApplicationGroup::get_Members, get_Members, security.iazapplicationgroup_members
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
 - IAzApplicationGroup.Members
 - IAzApplicationGroup.get_Members
 - AzApplicationGroup.Members
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::get_Members


## -description


The <b>Members</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of accounts that belong to the application group.

This property is read-only.


## -parameters


## -remarks



This property is ignored unless the <a href="https://msdn.microsoft.com/dc100895-4cfb-4e02-97bc-5c99bf26fbe2">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. 



