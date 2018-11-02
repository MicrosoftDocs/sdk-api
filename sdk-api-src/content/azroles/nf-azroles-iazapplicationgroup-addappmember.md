---
UID: NF:azroles.IAzApplicationGroup.AddAppMember
title: IAzApplicationGroup::AddAppMember
author: windows-sdk-content
description: Adds the specified IAzApplicationGroup object to the list of application groups that belong to this application group.
old-location: security\iazapplicationgroup_addappmember.htm
tech.root: secauthz
ms.assetid: 35b6c928-0c11-420d-8ba7-f28b0c67f55d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddAppMember, AddAppMember method [Security], AddAppMember method [Security],AzApplicationGroup object, AddAppMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddAppMember method, IAzApplicationGroup interface [Security],AddAppMember method, IAzApplicationGroup.AddAppMember, IAzApplicationGroup::AddAppMember, azroles/IAzApplicationGroup::AddAppMember, security.iazapplicationgroup_addappmember
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
 - IAzApplicationGroup.AddAppMember
 - AzApplicationGroup.AddAppMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::AddAppMember


## -description


The <b>AddAppMember</b> method adds the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to the list of application groups that belong to this application group.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/a42fb625-d04e-4884-b644-2007f6dc52ba">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to add to the list of the application groups that belong to this application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that belong to this application group, use the <a href="https://msdn.microsoft.com/74239ac2-b6ea-4839-b4c5-7a77d454aa0b">AppMembers</a> property.

You must call the <a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">Submit</a> method to persist any changes made by this method.



