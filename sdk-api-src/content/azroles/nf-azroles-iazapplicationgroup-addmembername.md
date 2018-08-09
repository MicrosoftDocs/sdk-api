---
UID: NF:azroles.IAzApplicationGroup.AddMemberName
title: IAzApplicationGroup::AddMemberName
author: windows-sdk-content
description: Adds the specified account name to the list of accounts that belong to the application group.
old-location: security\iazapplicationgroup_addmembername.htm
old-project: secauthz
ms.assetid: 148be96b-be8d-4ad7-a5ad-f22599114cfa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddMemberName, AddMemberName method [Security], AddMemberName method [Security],AzApplicationGroup object, AddMemberName method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddMemberName method, IAzApplicationGroup interface [Security],AddMemberName method, IAzApplicationGroup.AddMemberName, IAzApplicationGroup::AddMemberName, azroles/IAzApplicationGroup::AddMemberName, security.iazapplicationgroup_addmembername
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
 - IAzApplicationGroup.AddMemberName
 - AzApplicationGroup.AddMemberName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::AddMemberName


## -description


The <b>AddMemberName</b> method adds the specified account name to the list of  accounts that belong to the application group.


## -parameters




### -param bstrProp [in]

String that contains the account name to add to the list of accounts that belong to the application group. The account name must be in user principal name (UPN) format. The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of account names of  accounts that belong to this application group, use the <a href="https://msdn.microsoft.com/bdd6f88f-ea06-4075-b563-d0c7707107f8">MembersName</a> property.

You must call the <a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">Submit</a> method to persist any changes made by this method.



