---
UID: NF:azroles.IAzApplicationGroup.DeleteAppMember
title: IAzApplicationGroup::DeleteAppMember
author: windows-sdk-content
description: Removes the specified IAzApplicationGroup object from the list of application groups that belong to this application group.
old-location: security\iazapplicationgroup_deleteappmember.htm
tech.root: secauthz
ms.assetid: 856d9b18-927a-462a-b238-78b704bcc58b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: AzApplicationGroup object [Security],DeleteAppMember method, DeleteAppMember, DeleteAppMember method [Security], DeleteAppMember method [Security],AzApplicationGroup object, DeleteAppMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteAppMember method, IAzApplicationGroup.DeleteAppMember, IAzApplicationGroup::DeleteAppMember, azroles/IAzApplicationGroup::DeleteAppMember, security.iazapplicationgroup_deleteappmember
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
 - IAzApplicationGroup.DeleteAppMember
 - AzApplicationGroup.DeleteAppMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::DeleteAppMember


## -description


The <b>DeleteAppMember</b> method removes the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object from the list of application groups that belong to this application group.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/a42fb625-d04e-4884-b644-2007f6dc52ba">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to remove from the list of  application groups that belong to this application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that belong to this application group, use the <a href="https://msdn.microsoft.com/74239ac2-b6ea-4839-b4c5-7a77d454aa0b">AppMembers</a> property.



