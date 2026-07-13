---
UID: NF:appxpackaging.IAppxEncryptionFactory5.CreateEncryptedBundleReader2
tech.root: appxpkg
title: IAppxEncryptionFactory5::CreateEncryptedBundleReader2
ms.date: 02/13/2023
targetos: Windows
description: Creates a read-only bundle object to which encrypted Windows app packages can be added, with an optional parameter for specifying the expected digest for the encrypted bundle.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: appxpackaging.h
req.idl: AppxPackaging.idl
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - appxpackaging.h
api_name:
 - IAppxEncryptionFactory5::CreateEncryptedBundleReader2
f1_keywords:
 - IAppxEncryptionFactory5::CreateEncryptedBundleReader2
 - appxpackaging/IAppxEncryptionFactory5::CreateEncryptedBundleReader2
dev_langs:
 - c++
helpviewer_keywords:
 - CreateEncryptedBundleReader2
---

## -description

Creates a read-only bundle object to which encrypted Windows app packages can be added, with an optional parameter for specifying the expected digest for the encrypted bundle.

## -parameters

### -param inputStream [in]

A stream for reading the encrypted bundle.

### -param keyInfo [in]

 Key info containing the base encryption key and key ID for decrypting the bundle. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param expectedDigest [in.optional]

An LPCWSTR containing the expected digest, a hashed representation of the bundle file.

### -param bundleReader [out]

The created bundle reader.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |

## -remarks

Get the digest string for the *expecteDigest* parameter by calling [IAppxDigestProvider::GetDigest](nf-appxpackaging-iappxdigestprovider-getdigest.md).

## -see-also

