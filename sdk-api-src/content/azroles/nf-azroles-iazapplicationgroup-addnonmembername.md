---
UID: NF:azroles.IAzApplicationGroup.AddNonMemberName
title: IAzApplicationGroup::AddNonMemberName
author: windows-sdk-content
description: Adds the specified account name to the list of accounts that are refused membership in the application group.
old-location: security\iazapplicationgroup_addnonmembername.htm
tech.root: SecAuthZ
ms.assetid: 56bde3d9-f4f7-449d-a080-5215dda940a0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddNonMemberName, AddNonMemberName method [Security], AddNonMemberName method [Security],AzApplicationGroup object, AddNonMemberName method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddNonMemberName method, IAzApplicationGroup interface [Security],AddNonMemberName method, IAzApplicationGroup.AddNonMemberName, IAzApplicationGroup::AddNonMemberName, azroles/IAzApplicationGroup::AddNonMemberName, security.iazapplicationgroup_addnonmembername
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
 - IAzApplicationGroup.AddNonMemberName
 - AzApplicationGroup.AddNonMemberName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::AddNonMemberName


## -description


The <b>AddNonMemberName</b> method adds the specified account name to the list of  accounts that are refused membership in the application group.


## -parameters




### -param bstrProp [in]

String that contains the SID to add to the list of accounts that are refused membership in the application group. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



The application group will never have an  account added using this method as a member, even if that account is specified directly or indirectly by the <a href="https://msdn.microsoft.com/1370fe81-a729-477e-a500-1823abb713e1">Members</a> property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

To view the list of account names of  accounts that are refused membership in this application group, use the <a href="https://msdn.microsoft.com/d78556ae-0d22-4df0-b850-dd7077fa3f85">NonMembersName</a> property.

You must call the <a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">Submit</a> method to persist any changes made by this method.



