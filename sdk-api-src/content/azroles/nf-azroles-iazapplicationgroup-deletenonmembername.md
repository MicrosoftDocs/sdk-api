---
UID: NF:azroles.IAzApplicationGroup.DeleteNonMemberName
title: IAzApplicationGroup::DeleteNonMemberName
author: windows-sdk-content
description: Removes the specified account name from the list of accounts that are refused membership in the application group.
old-location: security\iazapplicationgroup_deletenonmembername.htm
old-project: SecAuthZ
ms.assetid: 8011e55a-1e62-45a6-a91c-07a488384d84
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: AzApplicationGroup object [Security],DeleteNonMemberName method, DeleteNonMemberName, DeleteNonMemberName method [Security], DeleteNonMemberName method [Security],AzApplicationGroup object, DeleteNonMemberName method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteNonMemberName method, IAzApplicationGroup.DeleteNonMemberName, IAzApplicationGroup::DeleteNonMemberName, azroles/IAzApplicationGroup::DeleteNonMemberName, security.iazapplicationgroup_deletenonmembername
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
 - IAzApplicationGroup.DeleteNonMemberName
 - AzApplicationGroup.DeleteNonMemberName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::DeleteNonMemberName


## -description


The <b>DeleteNonMemberName</b> method removes the specified account name from the list of  accounts that are refused membership in the application group.


## -parameters




### -param bstrProp [in]

String that contains the account name to remove from the list of   accounts that are refused membership in the application group. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of account names of accounts that are refused membership in this application group, use the <a href="https://msdn.microsoft.com/d78556ae-0d22-4df0-b850-dd7077fa3f85">NonMembersName</a> property.



