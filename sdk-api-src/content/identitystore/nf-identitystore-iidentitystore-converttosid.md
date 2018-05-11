---
UID: NF:identitystore.IIdentityStore.ConvertToSid
title: IIdentityStore::ConvertToSid
author: windows-driver-content
description: Retrieves the security identifier (SID) associated with the specified identity and identity provider.
old-location: security\iidentitystore_converttosid.htm
old-project: SecAuthN
ms.assetid: 484365a9-aeaf-453f-9a5b-6f88b79f8a35
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ConvertToSid, ConvertToSid method [Security], ConvertToSid method [Security],IIdentityStore interface, IIdentityStore interface [Security],ConvertToSid method, IIdentityStore.ConvertToSid, IIdentityStore::ConvertToSid, identitystore/IIdentityStore::ConvertToSid, security.iidentitystore_converttosid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IDENTITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Identitystore.h
api_name:
-	IIdentityStore.ConvertToSid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityStore::ConvertToSid


## -description


The <b>ConvertToSid</b> method retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) associated with the specified identity and identity provider.


## -parameters




### -param lpszUniqueID [in]

The identity for which to retrieve the SID.


### -param ProviderGUID [in]

The GUID of the identity provider.


### -param cbSid [in]

The size, in bytes, of the buffer pointed to by the <i>pSid</i> parameter.


### -param pSid [in, out]

A pointer to the SID this method retrieves.


### -param pcbRequiredSid [out]

The required length, in bytes,  of the <i>pSid</i> buffer.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6">IIdentityStore</a>
 

 

