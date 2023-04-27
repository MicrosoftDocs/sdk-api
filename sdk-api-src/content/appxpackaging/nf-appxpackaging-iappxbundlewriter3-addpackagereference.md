---
UID: NF:appxpackaging.IAppxBundleWriter3.AddPackageReference
title: IAppxBundleWriter3::AddPackageReference (appxpackaging.h)
description: Adds a reference to an optional app package or a payload file within an app bundle. (IAppxBundleWriter3.AddPackageReference)
helpviewer_keywords: ["AddPackageReference","AddPackageReference method [App packaging and management]","AddPackageReference method [App packaging and management]","IAppxBundleWriter3 interface","IAppxBundleWriter3 interface [App packaging and management]","AddPackageReference method","IAppxBundleWriter3.AddPackageReference","IAppxBundleWriter3::AddPackageReference","appxpackaging/IAppxBundleWriter3::AddPackageReference","appxpkg.iappxbundlewriter3_addpackagereference"]
old-location: appxpkg\iappxbundlewriter3_addpackagereference.htm
tech.root: appxpkg
ms.assetid: 99969971-9153-47C9-AF9C-7BF1D56EC54D
ms.date: 12/05/2018
ms.keywords: AddPackageReference, AddPackageReference method [App packaging and management], AddPackageReference method [App packaging and management],IAppxBundleWriter3 interface, IAppxBundleWriter3 interface [App packaging and management],AddPackageReference method, IAppxBundleWriter3.AddPackageReference, IAppxBundleWriter3::AddPackageReference, appxpackaging/IAppxBundleWriter3::AddPackageReference, appxpkg.iappxbundlewriter3_addpackagereference
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
 - IAppxBundleWriter3::AddPackageReference
 - appxpackaging/IAppxBundleWriter3::AddPackageReference
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
 - IAppxBundleWriter3.AddPackageReference
---

# IAppxBundleWriter3::AddPackageReference


## -description

Adds a reference to an optional app package or a payload file within an app bundle.

## -parameters

### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.

### -param inputStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of <i>fileName</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

By adding a reference to a payload file or optional app package to an app bundle, the overall size of the bundle is reduced.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter3">IAppxBundleWriter3</a>
