---
UID: NF:appxpackaging.IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted
title: IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted (appxpackaging.h)
description: Encrypts a new payload package to the bundle. (IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted)
helpviewer_keywords: ["AddPayloadPackageEncrypted","AddPayloadPackageEncrypted method [App packaging and management]","AddPayloadPackageEncrypted method [App packaging and management]","IAppxEncryptedBundleWriter3 interface","IAppxEncryptedBundleWriter3 interface [App packaging and management]","AddPayloadPackageEncrypted method","IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted","IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted","appxpackaging/IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted","appxpkg.iappxencryptedbundlewriter3_addpayloadpackageencrypted"]
old-location: appxpkg\iappxencryptedbundlewriter3_addpayloadpackageencrypted.htm
tech.root: appxpkg
ms.assetid: DB20D7FE-BB30-4E66-9617-BDDF1E00BB6A
ms.date: 12/05/2018
ms.keywords: AddPayloadPackageEncrypted, AddPayloadPackageEncrypted method [App packaging and management], AddPayloadPackageEncrypted method [App packaging and management],IAppxEncryptedBundleWriter3 interface, IAppxEncryptedBundleWriter3 interface [App packaging and management],AddPayloadPackageEncrypted method, IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted, IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted, appxpackaging/IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted, appxpkg.iappxencryptedbundlewriter3_addpayloadpackageencrypted
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
 - IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted
 - appxpackaging/IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted
---

# IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted


## -description

Encrypts a new payload package to the bundle.

## -parameters

### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.

### -param packageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of <i>fileName</i>.

### -param isDefaultApplicablePackage [in]

A flag for whether this package is a default applicable package.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedbundlewriter3">IAppxEncryptedBundleWriter3</a>
