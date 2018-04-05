---
UID: NF:azroles.IAzScope.AddPolicyReaderName
title: IAzScope::AddPolicyReaderName method
author: windows-driver-content
description: The AddPolicyReaderName method of IAzScope adds the specified account name to the list of principals that act as policy readers.
old-location: security\iazscope_addpolicyreadername.htm
old-project: SecAuthZ
ms.assetid: 6beb02cb-7977-4f3f-b806-420c81f6f0b5
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AddPolicyReaderName method [Security], AddPolicyReaderName method [Security], AzScope object, AddPolicyReaderName method [Security], IAzScope interface, AddPolicyReaderName,IAzScope.AddPolicyReaderName, AzScope object [Security], AddPolicyReaderName method, IAzScope, IAzScope interface [Security], AddPolicyReaderName method, IAzScope::AddPolicyReaderName, azroles/IAzScope::AddPolicyReaderName, security.iazscope_addpolicyreadername
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
-	IAzScope.AddPolicyReaderName
-	AzScope.AddPolicyReaderName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::AddPolicyReaderName method


## -description


The <b>AddPolicyReaderName</b> method adds the specified account name to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Account name to add to the list of policy readers. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://msdn.microsoft.com/4f56ee3f-f987-4569-9e19-c13ab3ff100a">PolicyReadersName</a> property.

You must call the <a href="https://msdn.microsoft.com/c06f1994-71d9-4867-a5ed-8fa90206994f">Submit</a> method to persist any changes made by this method.



