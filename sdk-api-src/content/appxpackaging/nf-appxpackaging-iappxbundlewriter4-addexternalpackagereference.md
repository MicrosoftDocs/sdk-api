---
UID: NF:appxpackaging.IAppxBundleWriter4.AddExternalPackageReference
title: IAppxBundleWriter4::AddExternalPackageReference (appxpackaging.h)
description: Adds a reference within the package bundle to an external app package.
helpviewer_keywords: ["AddExternalPackageReference","AddExternalPackageReference method [App packaging and management]","AddExternalPackageReference method [App packaging and management]","IAppxBundleWriter4 interface","IAppxBundleWriter4 interface [App packaging and management]","AddExternalPackageReference method","IAppxBundleWriter4.AddExternalPackageReference","IAppxBundleWriter4::AddExternalPackageReference","appxpackaging/IAppxBundleWriter4::AddExternalPackageReference","appxpkg.iappxbundlewriter4_addexternalpackagereference"]
old-location: appxpkg\iappxbundlewriter4_addexternalpackagereference.htm
tech.root: appxpkg
ms.assetid: 2C655FF8-93F5-4132-8D61-1C47DB317043
ms.date: 12/05/2018
ms.keywords: AddExternalPackageReference, AddExternalPackageReference method [App packaging and management], AddExternalPackageReference method [App packaging and management],IAppxBundleWriter4 interface, IAppxBundleWriter4 interface [App packaging and management],AddExternalPackageReference method, IAppxBundleWriter4.AddExternalPackageReference, IAppxBundleWriter4::AddExternalPackageReference, appxpackaging/IAppxBundleWriter4::AddExternalPackageReference, appxpkg.iappxbundlewriter4_addexternalpackagereference
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
 - IAppxBundleWriter4::AddExternalPackageReference
 - appxpackaging/IAppxBundleWriter4::AddExternalPackageReference
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
 - IAppxBundleWriter4.AddExternalPackageReference
---

# IAppxBundleWriter4::AddExternalPackageReference


## -description

Adds a reference within the package bundle to an external app package.

## -parameters

### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.

### -param inputStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of <i>fileName</i>.

### -param isDefaultApplicablePackage [in]

A flag for whether this package is a default applicable package.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo2-getisdefaultapplicablepackage">GetIsDefaultApplicablePackage</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter4">IAppxBundleWriter4</a>