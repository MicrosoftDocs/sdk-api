---
UID: NF:appxpackaging.IAppxBundleWriter4.AddPayloadPackage
title: IAppxBundleWriter4::AddPayloadPackage (appxpackaging.h)
description: Adds a new app package to the bundle. (IAppxBundleWriter4.AddPayloadPackage)
helpviewer_keywords: ["AddPayloadPackage","AddPayloadPackage method [App packaging and management]","AddPayloadPackage method [App packaging and management]","IAppxBundleWriter4 interface","IAppxBundleWriter4 interface [App packaging and management]","AddPayloadPackage method","IAppxBundleWriter4.AddPayloadPackage","IAppxBundleWriter4::AddPayloadPackage","appxpackaging/IAppxBundleWriter4::AddPayloadPackage","appxpkg.iappxbundlewriter4_addpayloadpackage"]
old-location: appxpkg\iappxbundlewriter4_addpayloadpackage.htm
tech.root: appxpkg
ms.assetid: 5D313F6C-F2EC-42A4-A4A8-8026E7DBF67B
ms.date: 12/05/2018
ms.keywords: AddPayloadPackage, AddPayloadPackage method [App packaging and management], AddPayloadPackage method [App packaging and management],IAppxBundleWriter4 interface, IAppxBundleWriter4 interface [App packaging and management],AddPayloadPackage method, IAppxBundleWriter4.AddPayloadPackage, IAppxBundleWriter4::AddPayloadPackage, appxpackaging/IAppxBundleWriter4::AddPayloadPackage, appxpkg.iappxbundlewriter4_addpayloadpackage
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
 - IAppxBundleWriter4::AddPayloadPackage
 - appxpackaging/IAppxBundleWriter4::AddPayloadPackage
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
 - IAppxBundleWriter4.AddPayloadPackage
---

# IAppxBundleWriter4::AddPayloadPackage


## -description

Adds a new app package to the bundle.

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

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter4">IAppxBundleWriter4</a>
