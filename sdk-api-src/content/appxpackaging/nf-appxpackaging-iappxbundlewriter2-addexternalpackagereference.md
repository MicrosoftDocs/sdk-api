---
UID: NF:appxpackaging.IAppxBundleWriter2.AddExternalPackageReference
title: IAppxBundleWriter2::AddExternalPackageReference (appxpackaging.h)
description: Adds a reference to an external package to the package bundle.
helpviewer_keywords: ["AddExternalPackageReference","AddExternalPackageReference method [App packaging and management]","AddExternalPackageReference method [App packaging and management]","IAppxBundleWriter2 interface","IAppxBundleWriter2 interface [App packaging and management]","AddExternalPackageReference method","IAppxBundleWriter2.AddExternalPackageReference","IAppxBundleWriter2::AddExternalPackageReference","appxpackaging/IAppxBundleWriter2::AddExternalPackageReference","appxpkg.iappxbundlewriter2_addexternalpackagereference"]
old-location: appxpkg\iappxbundlewriter2_addexternalpackagereference.htm
tech.root: appxpkg
ms.assetid: 09297744-69E4-45D6-BA5C-A3B28130C6CC
ms.date: 12/05/2018
ms.keywords: AddExternalPackageReference, AddExternalPackageReference method [App packaging and management], AddExternalPackageReference method [App packaging and management],IAppxBundleWriter2 interface, IAppxBundleWriter2 interface [App packaging and management],AddExternalPackageReference method, IAppxBundleWriter2.AddExternalPackageReference, IAppxBundleWriter2::AddExternalPackageReference, appxpackaging/IAppxBundleWriter2::AddExternalPackageReference, appxpkg.iappxbundlewriter2_addexternalpackagereference
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
 - IAppxBundleWriter2::AddExternalPackageReference
 - appxpackaging/IAppxBundleWriter2::AddExternalPackageReference
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
 - IAppxBundleWriter2.AddExternalPackageReference
---

# IAppxBundleWriter2::AddExternalPackageReference


## -description

Adds a reference to an external package to the package bundle.

## -parameters

### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.

### -param inputStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of <i>fileName</i>.
          The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter2">IAppxBundleWriter2</a>