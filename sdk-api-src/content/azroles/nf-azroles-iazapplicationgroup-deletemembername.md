---
UID: NF:azroles.IAzApplicationGroup.DeleteMemberName
title: IAzApplicationGroup::DeleteMemberName (azroles.h)
author: windows-sdk-content
description: Removes the specified account name from the list of accounts that belong to the application group.
old-location: security\iazapplicationgroup_deletemembername.htm
tech.root: SecAuthZ
ms.assetid: 3b3a8aee-b1ef-464a-9b67-80b703d41d69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],DeleteMemberName method, DeleteMemberName, DeleteMemberName method [Security], DeleteMemberName method [Security],AzApplicationGroup object, DeleteMemberName method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteMemberName method, IAzApplicationGroup.DeleteMemberName, IAzApplicationGroup::DeleteMemberName, azroles/IAzApplicationGroup::DeleteMemberName, security.iazapplicationgroup_deletemembername
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
 - IAzApplicationGroup.DeleteMemberName
 - AzApplicationGroup.DeleteMemberName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup::DeleteMemberName


## -description


The <b>DeleteMemberName</b> method removes  the specified account name from the list of  accounts that belong to the application group.


## -parameters




### -param bstrProp [in]

String that contains the account name to remove from the list of   accounts that belong to the application group. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of account names of  accounts that belong to this application group, use the <a href="https://msdn.microsoft.com/bdd6f88f-ea06-4075-b563-d0c7707107f8">MembersName</a> property.



