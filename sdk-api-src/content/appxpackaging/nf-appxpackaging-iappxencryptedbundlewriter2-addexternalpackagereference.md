---
UID: NF:appxpackaging.IAppxEncryptedBundleWriter2.AddExternalPackageReference
title: IAppxEncryptedBundleWriter2::AddExternalPackageReference (appxpackaging.h)
description: Adds a reference within the encrypted package bundle to an external app package. (IAppxEncryptedBundleWriter2.AddExternalPackageReference)
helpviewer_keywords: ["AddExternalPackageReference","AddExternalPackageReference method [App packaging and management]","AddExternalPackageReference method [App packaging and management]","IAppxEncryptedBundleWriter2 interface","IAppxEncryptedBundleWriter2 interface [App packaging and management]","AddExternalPackageReference method","IAppxEncryptedBundleWriter2.AddExternalPackageReference","IAppxEncryptedBundleWriter2::AddExternalPackageReference","appxpackaging/IAppxEncryptedBundleWriter2::AddExternalPackageReference","appxpkg.iappxencryptedbundlewriter2_addexternalpackagereference"]
old-location: appxpkg\iappxencryptedbundlewriter2_addexternalpackagereference.htm
tech.root: appxpkg
ms.assetid: F1572E99-17C0-4239-9F95-47880CC50C64
ms.date: 12/05/2018
ms.keywords: AddExternalPackageReference, AddExternalPackageReference method [App packaging and management], AddExternalPackageReference method [App packaging and management],IAppxEncryptedBundleWriter2 interface, IAppxEncryptedBundleWriter2 interface [App packaging and management],AddExternalPackageReference method, IAppxEncryptedBundleWriter2.AddExternalPackageReference, IAppxEncryptedBundleWriter2::AddExternalPackageReference, appxpackaging/IAppxEncryptedBundleWriter2::AddExternalPackageReference, appxpkg.iappxencryptedbundlewriter2_addexternalpackagereference
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
 - IAppxEncryptedBundleWriter2::AddExternalPackageReference
 - appxpackaging/IAppxEncryptedBundleWriter2::AddExternalPackageReference
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
 - IAppxEncryptedBundleWriter2.AddExternalPackageReference
---

# IAppxEncryptedBundleWriter2::AddExternalPackageReference


## -description

Adds a reference within the encrypted package bundle to an external app package.

## -parameters

### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.

### -param inputStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of <i>fileName</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedbundlewriter2">IAppxEncryptedBundleWriter2</a>
