---
UID: NF:appxpackaging.IAppxEncryptionFactory5.CreateEncryptedPackageReader2
tech.root: appxpkg
title: IAppxEncryptionFactory5::CreateEncryptedPackageReader2
ms.date: 02/13/2023
targetos: Windows
description: Creates a new instance of IAppxPackageReader for reading encrypted packages, with an optional parameter for specifying the expected digest for the package.
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
 - IAppxEncryptionFactory5::CreateEncryptedPackageReader2
f1_keywords:
 - IAppxEncryptionFactory5::CreateEncryptedPackageReader2
 - appxpackaging/IAppxEncryptionFactory5::CreateEncryptedPackageReader2
dev_langs:
 - c++
helpviewer_keywords:
 - CreateEncryptedPackageReader2
---

## -description

Creates a new instance of [IAppxPackageReader](nn-appxpackaging-iappxpackagereader.md) for reading encrypted packages, with an optional parameter for specifying the expected digest for the package.

## -parameters

### -param inputStream

A stream for reading the encrypted package.

### -param keyInfo

Key info containing the base encryption key and key ID for decrypting the package. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param expectedDigest

An LPCWSTR containing the expected digest, a hashed representation of the package file.

### -param packageReader

The created package reader.

## -returns

If the method succeeds, it returns **S_OK**. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |

## -remarks

Get the digest string for the *expecteDigest* parameter by calling [IAppxDigestProvider::GetDigest](nf-appxpackaging-iappxdigestprovider-getdigest.md).

## -see-also

