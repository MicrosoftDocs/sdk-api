---
UID: NF:appxpackaging.IAppxDigestProvider.GetDigest
tech.root: appxpkg
title: IAppxDigestProvider::GetDigest
ms.date: 02/16/2023
targetos: Windows
description: Receives a pointer to an LPWSTR containing the digest representation of the app packaging object object managed by the associated interface.
prerelease: false
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
 - IAppxDigestProvider::GetDigest
f1_keywords:
 - IAppxDigestProvider::GetDigest
 - appxpackaging/IAppxDigestProvider::GetDigest
dev_langs:
 - c++
helpviewer_keywords:
 - GetDigest
---

## -description

Retrieves the digest representation of the app packaging object managed by the associated interface.

## -parameters

### -param digest [out]

Receives a pointer to an LPWSTR containing the digest representation of the app packaging object object managed by the associated interface.

## -returns

Returns **S_OK** on success.

## -remarks

A digest string is a hashed representation of the contents of the associated object that can be used to verify that the contents of the object haven't changed between operations.

The **IAppxDigestProvider** interface can be obtained by calling **QueryInterface** on the objects returned by the following factory interfaces, as well as the corresponding methods in different versions of the factory interfaces, such as [IAppxFactory::CreatePackageReader](nf-appxpackaging-iappxfactory-createpackagereader.md): 

- [IAppxEncryptionFactory5](nn-appxpackaging-iappxencryptionfactory4.md)
- [IAppxBundleFactory2](nn-appxpackaging-iappxbundlefactory2.md)
- [IAppxFactory3](nn-appxpackaging-iappxfactory3.md)


## -see-also

