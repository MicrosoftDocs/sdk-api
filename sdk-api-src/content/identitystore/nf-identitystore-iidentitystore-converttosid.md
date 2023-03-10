---
UID: NF:identitystore.IIdentityStore.ConvertToSid
title: IIdentityStore::ConvertToSid (identitystore.h)
description: Retrieves the security identifier (SID) associated with the specified identity and identity provider.
helpviewer_keywords: ["ConvertToSid","ConvertToSid method [Security]","ConvertToSid method [Security]","IIdentityStore interface","IIdentityStore interface [Security]","ConvertToSid method","IIdentityStore.ConvertToSid","IIdentityStore::ConvertToSid","identitystore/IIdentityStore::ConvertToSid","security.iidentitystore_converttosid"]
old-location: security\iidentitystore_converttosid.htm
tech.root: security
ms.assetid: 484365a9-aeaf-453f-9a5b-6f88b79f8a35
ms.date: 12/05/2018
ms.keywords: ConvertToSid, ConvertToSid method [Security], ConvertToSid method [Security],IIdentityStore interface, IIdentityStore interface [Security],ConvertToSid method, IIdentityStore.ConvertToSid, IIdentityStore::ConvertToSid, identitystore/IIdentityStore::ConvertToSid, security.iidentitystore_converttosid
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIdentityStore::ConvertToSid
 - identitystore/IIdentityStore::ConvertToSid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identitystore.h
api_name:
 - IIdentityStore.ConvertToSid
---

# IIdentityStore::ConvertToSid


## -description

The <b>ConvertToSid</b> method retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) associated with the specified identity and identity provider.

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

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identitystore/nn-identitystore-iidentitystore">IIdentityStore</a>