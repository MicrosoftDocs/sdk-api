---
UID: NF:azroles.IAzApplication.DeletePolicyReaderName
title: IAzApplication::DeletePolicyReaderName
author: windows-sdk-content
description: Removes the specified account name from the list of principals that act as policy readers.
old-location: security\iazapplication_deletepolicyreadername.htm
tech.root: secauthz
ms.assetid: 1948fb2d-a1ca-4f66-889d-d00f8f265ba5
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: AzApplication object [Security],DeletePolicyReaderName method, DeletePolicyReaderName, DeletePolicyReaderName method [Security], DeletePolicyReaderName method [Security],AzApplication object, DeletePolicyReaderName method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePolicyReaderName method, IAzApplication.DeletePolicyReaderName, IAzApplication::DeletePolicyReaderName, azroles/IAzApplication::DeletePolicyReaderName, security.iazapplication_deletepolicyreadername
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
 - IAzApplication.DeletePolicyReaderName
 - AzApplication.DeletePolicyReaderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::DeletePolicyReaderName


## -description


The <b>DeletePolicyReaderName</b> method removes the specified account name from the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

The account name to remove from the list of policy readers. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the format of "ExampleDomain\UserName". If the domain is not  in the "ExampleDomain\UserName" format, the <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://msdn.microsoft.com/e6ed4504-0df1-438b-87c7-1861264d02bd">PolicyReadersName</a> property.



