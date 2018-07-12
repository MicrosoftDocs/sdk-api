---
UID: NF:azroles.IAzApplicationGroup.AddNonMember
title: IAzApplicationGroup::AddNonMember
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of accounts that are refused membership in the application group.
old-location: security\iazapplicationgroup_addnonmember.htm
old-project: secauthz
ms.assetid: a61f0b97-cd8a-40e5-b2ef-8eb48359fead
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: AddNonMember, AddNonMember method [Security], AddNonMember method [Security],AzApplicationGroup object, AddNonMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddNonMember method, IAzApplicationGroup interface [Security],AddNonMember method, IAzApplicationGroup.AddNonMember, IAzApplicationGroup::AddNonMember, azroles/IAzApplicationGroup::AddNonMember, security.iazapplicationgroup_addnonmember
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzApplicationGroup.AddNonMember
 - AzApplicationGroup.AddNonMember
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::AddNonMember


## -description


The <b>AddNonMember</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of  accounts that are refused membership in the application group.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to add to the list of  accounts that are refused membership in the application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



The application group will never have an  account added using this method as a member, even if that account is specified directly or indirectly by the <a href="https://msdn.microsoft.com/1370fe81-a729-477e-a500-1823abb713e1">Members</a> property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

To view the list of SIDs of accounts that are refused membership in this application group in text form, use the <a href="https://msdn.microsoft.com/43bdd205-4750-4ff6-8063-8de2c5962b09">NonMembers</a> property.

You must call the <a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">Submit</a> method to persist any changes made by this method.



