---
UID: NF:azroles.IAzRole.AddMemberName
title: IAzRole::AddMemberName method
author: windows-driver-content
description: Adds the specified account name to the list of accounts that belong to the role.
old-location: security\iazrole_addmembername.htm
old-project: SecAuthZ
ms.assetid: fc2ca62e-40b1-4b09-a129-50d6162c6807
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AddMemberName method [Security], AddMemberName method [Security], AzRole object, AddMemberName method [Security], IAzRole interface, AddMemberName,IAzRole.AddMemberName, AzRole object [Security], AddMemberName method, IAzRole, IAzRole interface [Security], AddMemberName method, IAzRole::AddMemberName, azroles/IAzRole::AddMemberName, security.iazrole_addmembername
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzRole.AddMemberName
-	AzRole.AddMemberName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::AddMemberName method


## -description


The <b>AddMemberName</b> method adds the specified account name to the list of  accounts that belong to the role.


## -parameters




### -param bstrProp [in]

String that contains the account name to add to the list of   accounts that belong to the role. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the  "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of account names of accounts that belong to this role, use the <a href="https://msdn.microsoft.com/defaefa8-2d76-49c6-bd1c-8b386f9dc5f1">MembersName</a> property.

You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



