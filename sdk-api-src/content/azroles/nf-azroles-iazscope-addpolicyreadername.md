---
UID: NF:azroles.IAzScope.AddPolicyReaderName
title: IAzScope::AddPolicyReaderName
author: windows-sdk-content
description: The AddPolicyReaderName method of IAzScope adds the specified account name to the list of principals that act as policy readers.
old-location: security\iazscope_addpolicyreadername.htm
tech.root: SecAuthZ
ms.assetid: 6beb02cb-7977-4f3f-b806-420c81f6f0b5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddPolicyReaderName, AddPolicyReaderName method [Security], AddPolicyReaderName method [Security],AzScope object, AddPolicyReaderName method [Security],IAzScope interface, AzScope object [Security],AddPolicyReaderName method, IAzScope interface [Security],AddPolicyReaderName method, IAzScope.AddPolicyReaderName, IAzScope::AddPolicyReaderName, azroles/IAzScope::AddPolicyReaderName, security.iazscope_addpolicyreadername
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
 - IAzScope.AddPolicyReaderName
 - AzScope.AddPolicyReaderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::AddPolicyReaderName


## -description


The <b>AddPolicyReaderName</b> method adds the specified account name to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Account name to add to the list of policy readers. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="https://msdn.microsoft.com/en-us/library/Aa379159(v=VS.85).aspx">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/en-us/library/Aa377880(v=VS.85).aspx">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://msdn.microsoft.com/en-us/library/Aa378361(v=VS.85).aspx">PolicyReadersName</a> property.

You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa378364(v=VS.85).aspx">Submit</a> method to persist any changes made by this method.



