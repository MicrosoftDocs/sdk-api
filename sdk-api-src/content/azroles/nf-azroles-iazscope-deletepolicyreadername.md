---
UID: NF:azroles.IAzScope.DeletePolicyReaderName
title: IAzScope::DeletePolicyReaderName
author: windows-sdk-content
description: The DeletePolicyReaderName method of IAzScope removes the specified account name from the list of principals that act as policy readers.
old-location: security\iazscope_deletepolicyreadername.htm
tech.root: SecAuthZ
ms.assetid: e65af2a2-c7f7-483c-af05-342075218158
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AzScope object [Security],DeletePolicyReaderName method, DeletePolicyReaderName, DeletePolicyReaderName method [Security], DeletePolicyReaderName method [Security],AzScope object, DeletePolicyReaderName method [Security],IAzScope interface, IAzScope interface [Security],DeletePolicyReaderName method, IAzScope.DeletePolicyReaderName, IAzScope::DeletePolicyReaderName, azroles/IAzScope::DeletePolicyReaderName, security.iazscope_deletepolicyreadername
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
 - IAzScope.DeletePolicyReaderName
 - AzScope.DeletePolicyReaderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::DeletePolicyReaderName


## -description


The <b>DeletePolicyReaderName</b> method removes the specified account name from the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Account name to remove from the list of policy readers. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://msdn.microsoft.com/4f56ee3f-f987-4569-9e19-c13ab3ff100a">PolicyReadersName</a> property.



