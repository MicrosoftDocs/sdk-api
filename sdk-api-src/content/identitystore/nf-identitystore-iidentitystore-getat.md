---
UID: NF:identitystore.IIdentityStore.GetAt
title: IIdentityStore::GetAt
author: windows-sdk-content
description: Retrieves an IIdentityProvider interface pointer for the specified identity provider.
old-location: security\iidentitystore_getat.htm
old-project: SecAuthN
ms.assetid: c62212bf-852b-43fb-9abf-b85f4d15b305
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetAt, GetAt method [Security], GetAt method [Security],IIdentityStore interface, IIdentityStore interface [Security],GetAt method, IIdentityStore.GetAt, IIdentityStore::GetAt, identitystore/IIdentityStore::GetAt, security.iidentitystore_getat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: identitystore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IDENTITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Identitystore.h
api_name:
-	IIdentityStore.GetAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityStore::GetAt


## -description


The <b>GetAt</b> method retrieves an <a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a> interface pointer for the specified identity provider.


## -parameters




### -param dwProvider [in]

The index of the identity provider to retrieve.


### -param pProvGuid [in, out]

On output, this parameter receives a pointer to the GUID of the identity provider that this function retrieves.


### -param ppIdentityProvider [out]

A pointer to the <a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a> interface pointer that this method retrieves.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6">IIdentityStore</a>
 

 

