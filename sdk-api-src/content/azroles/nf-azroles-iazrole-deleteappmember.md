---
UID: NF:azroles.IAzRole.DeleteAppMember
title: IAzRole::DeleteAppMember
author: windows-sdk-content
description: Removes the specified IAzApplicationGroup object from the list of application groups that belong to the role.
old-location: security\iazrole_deleteappmember.htm
old-project: secauthz
ms.assetid: b2856d75-cf16-4eec-a0e1-2e9e9fff601e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzRole object [Security],DeleteAppMember method, DeleteAppMember, DeleteAppMember method [Security], DeleteAppMember method [Security],AzRole object, DeleteAppMember method [Security],IAzRole interface, IAzRole interface [Security],DeleteAppMember method, IAzRole.DeleteAppMember, IAzRole::DeleteAppMember, azroles/IAzRole::DeleteAppMember, security.iazrole_deleteappmember
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
 - IAzRole.DeleteAppMember
 - AzRole.DeleteAppMember
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::DeleteAppMember


## -description


The <b>DeleteAppMember</b> method removes the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object from the list of application groups that belong to the role.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/a42fb625-d04e-4884-b644-2007f6dc52ba">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to remove from the list of  application groups that belong to the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that belong to the role, use the <a href="https://msdn.microsoft.com/c41933d4-d3fe-485c-9249-e82d51c0bfc9">AppMembers</a> property.



