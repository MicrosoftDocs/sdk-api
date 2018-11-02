---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyReaderName
title: IAzAuthorizationStore::AddPolicyReaderName
author: windows-sdk-content
description: Adds the specified account name to the list of principals that act as policy readers.
old-location: security\azauthorizationstore_addpolicyreadername.htm
tech.root: secauthz
ms.assetid: 3b111542-61d6-4e5d-abf8-0af61161c885
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddPolicyReaderName, AddPolicyReaderName method [Security], AddPolicyReaderName method [Security],AzAuthorizationStore object, AddPolicyReaderName method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyReaderName method, IAzAuthorizationStore interface [Security],AddPolicyReaderName method, IAzAuthorizationStore.AddPolicyReaderName, IAzAuthorizationStore::AddPolicyReaderName, azroles/IAzAuthorizationStore::AddPolicyReaderName, security.azauthorizationstore_addpolicyreadername
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
 - AzAuthorizationStore.AddPolicyReaderName
 - IAzAuthorizationStore.AddPolicyReaderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::AddPolicyReaderName


## -description


The <b>AddPolicyReaderName</b> method adds the specified account name to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Account name to add to the list of policy readers. The account name must be in <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the  <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://msdn.microsoft.com/d550448e-a1ea-45f3-9151-affd4b8c0b14">PolicyReadersName</a> property.

You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



