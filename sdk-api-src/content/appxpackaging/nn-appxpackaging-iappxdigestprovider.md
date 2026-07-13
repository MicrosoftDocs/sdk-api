---
UID: NN:appxpackaging.IAppxDigestProvider
tech.root: appxpkg
title: IAppxDigestProvider
ms.date: 02/16/2023
targetos: Windows
description: Provides APIs for retrieving the digest string representation of an app packaging object.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: appxpackaging.h
req.idl: AppxPackaging.idl
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - appxpackaging.h
api_name:
 - IAppxDigestProvider
f1_keywords:
 - IAppxDigestProvider
 - appxpackaging/IAppxDigestProvider
dev_langs:
 - c++
helpviewer_keywords:
 - IAppxDigestProvider
---

## -description

Provides APIs for retrieving the digest string representation of an app packaging object.

## -remarks

The **IAppxDigestProvider** interface can be obtained by calling **QueryInterface** on the objects returned by the following factory interfaces, as well as the corresponding methods in different versions of the factory interfaces, such as [IAppxFactory::CreatePackageReader](nf-appxpackaging-iappxfactory-createpackagereader.md): 

- [IAppxEncryptionFactory5](nn-appxpackaging-iappxencryptionfactory4.md)
- [IAppxBundleFactory2](nn-appxpackaging-iappxbundlefactory2.md)
- [IAppxFactory3](nn-appxpackaging-iappxfactory3.md)



## -see-also

