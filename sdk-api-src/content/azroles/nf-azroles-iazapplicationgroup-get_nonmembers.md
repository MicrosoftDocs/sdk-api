---
UID: NF:azroles.IAzApplicationGroup.get_NonMembers
title: IAzApplicationGroup::get_NonMembers (azroles.h)
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs), in text form, of accounts that are refused membership in the application group.
old-location: security\iazapplicationgroup_nonmembers.htm
tech.root: SecAuthZ
ms.assetid: 43bdd205-4750-4ff6-8063-8de2c5962b09
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AzApplicationGroup object [Security],NonMembers property, IAzApplicationGroup interface [Security],NonMembers property, IAzApplicationGroup.NonMembers, IAzApplicationGroup.get_NonMembers, IAzApplicationGroup::NonMembers, IAzApplicationGroup::get_NonMembers, NonMembers property [Security], NonMembers property [Security],AzApplicationGroup object, NonMembers property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::NonMembers, azroles/IAzApplicationGroup::get_NonMembers, get_NonMembers, security.iazapplicationgroup_nonmembers
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
 - IAzApplicationGroup.NonMembers
 - IAzApplicationGroup.get_NonMembers
 - AzApplicationGroup.NonMembers
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::get_NonMembers


## -description


The <b>NonMembers</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of  accounts that are refused membership in  the application group.

This property is read-only.


## -parameters


## -remarks



The application group will never have an  account specified by this property as a member, even if that account is specified directly or indirectly by the <a href="https://msdn.microsoft.com/1370fe81-a729-477e-a500-1823abb713e1">Members</a> property.

This property is ignored unless the <a href="https://msdn.microsoft.com/dc100895-4cfb-4e02-97bc-5c99bf26fbe2">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.



