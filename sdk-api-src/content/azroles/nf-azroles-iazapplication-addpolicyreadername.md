---
UID: NF:azroles.IAzApplication.AddPolicyReaderName
title: IAzApplication::AddPolicyReaderName method
author: windows-driver-content
description: Adds the specified account name to the list of principals that act as policy readers.
old-location: security\iazapplication_addpolicyreadername.htm
old-project: SecAuthZ
ms.assetid: cc81527a-7a38-4c5c-857e-bedcda5a5ac3
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AddPolicyReaderName method [Security], AddPolicyReaderName method [Security], AzApplication object, AddPolicyReaderName method [Security], IAzApplication interface, AddPolicyReaderName,IAzApplication.AddPolicyReaderName, AzApplication object [Security], AddPolicyReaderName method, IAzApplication, IAzApplication interface [Security], AddPolicyReaderName method, IAzApplication::AddPolicyReaderName, azroles/IAzApplication::AddPolicyReaderName, security.iazapplication_addpolicyreadername
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
-	IAzApplication.AddPolicyReaderName
-	AzApplication.AddPolicyReaderName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::AddPolicyReaderName method


## -description


The <b>AddPolicyReaderName</b> method adds the specified account name to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Account name to add to the list of policy readers. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://msdn.microsoft.com/e6ed4504-0df1-438b-87c7-1861264d02bd">PolicyReadersName</a> property.

You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



