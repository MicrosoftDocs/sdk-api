---
UID: NF:azroles.IAzApplicationGroup.DeleteAppNonMember
title: IAzApplicationGroup::DeleteAppNonMember
author: windows-sdk-content
description: Removes the specified IAzApplicationGroup object from the list of application groups that are refused membership in this application group.
old-location: security\iazapplicationgroup_deleteappnonmember.htm
old-project: secauthz
ms.assetid: d78f3cd9-4ccb-47b7-98bd-5e69ebbb178c
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzApplicationGroup object [Security],DeleteAppNonMember method, DeleteAppNonMember, DeleteAppNonMember method [Security], DeleteAppNonMember method [Security],AzApplicationGroup object, DeleteAppNonMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteAppNonMember method, IAzApplicationGroup.DeleteAppNonMember, IAzApplicationGroup::DeleteAppNonMember, azroles/IAzApplicationGroup::DeleteAppNonMember, security.iazapplicationgroup_deleteappnonmember
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
 - IAzApplicationGroup.DeleteAppNonMember
 - AzApplicationGroup.DeleteAppNonMember
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::DeleteAppNonMember


## -description


The <b>DeleteAppNonMember</b> method removes the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object from the list of application groups that are refused membership in this application group.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/a42fb625-d04e-4884-b644-2007f6dc52ba">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to remove from the list of the application groups that are refused membership in this application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that are refused membership in this application group, use the <a href="https://msdn.microsoft.com/a85a9004-f3f5-44ce-a0d7-fa450af74917">AppNonMembers</a> property.



