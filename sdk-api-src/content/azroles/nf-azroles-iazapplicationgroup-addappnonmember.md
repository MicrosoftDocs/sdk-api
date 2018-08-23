---
UID: NF:azroles.IAzApplicationGroup.AddAppNonMember
title: IAzApplicationGroup::AddAppNonMember
author: windows-sdk-content
description: Adds the specified IAzApplicationGroup object to the list of application groups that are refused membership in this application group.
old-location: security\iazapplicationgroup_addappnonmember.htm
old-project: secauthz
ms.assetid: 31b8538f-afe1-4fd3-bf6f-6f3f0641fc2a
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AddAppNonMember, AddAppNonMember method [Security], AddAppNonMember method [Security],AzApplicationGroup object, AddAppNonMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddAppNonMember method, IAzApplicationGroup interface [Security],AddAppNonMember method, IAzApplicationGroup.AddAppNonMember, IAzApplicationGroup::AddAppNonMember, azroles/IAzApplicationGroup::AddAppNonMember, security.iazapplicationgroup_addappnonmember
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
 - IAzApplicationGroup.AddAppNonMember
 - AzApplicationGroup.AddAppNonMember
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::AddAppNonMember


## -description


The <b>AddAppNonMember</b> method adds the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to the list of application groups that are refused membership in this application group.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/a42fb625-d04e-4884-b644-2007f6dc52ba">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to add to the list of the application groups that are refused membership in this application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that are refused membership in this application group, use the <a href="https://msdn.microsoft.com/a85a9004-f3f5-44ce-a0d7-fa450af74917">AppNonMembers</a> property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

You must call the <a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">Submit</a> method to persist any changes made by this method.



