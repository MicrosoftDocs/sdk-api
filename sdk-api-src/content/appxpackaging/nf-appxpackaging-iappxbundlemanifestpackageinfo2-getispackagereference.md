---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo2.GetIsPackageReference
title: IAppxBundleManifestPackageInfo2::GetIsPackageReference (appxpackaging.h)
description: Determines whether a package is stored inside an app bundle, or if it's a reference to a package.
helpviewer_keywords: ["GetIsPackageReference","GetIsPackageReference method [App packaging and management]","GetIsPackageReference method [App packaging and management]","IAppxBundleManifestPackageInfo2 interface","IAppxBundleManifestPackageInfo2 interface [App packaging and management]","GetIsPackageReference method","IAppxBundleManifestPackageInfo2.GetIsPackageReference","IAppxBundleManifestPackageInfo2::GetIsPackageReference","appxpackaging/IAppxBundleManifestPackageInfo2::GetIsPackageReference","appxpkg.iappxbundlemanifestpackageinfo2_getispackagereference"]
old-location: appxpkg\iappxbundlemanifestpackageinfo2_getispackagereference.htm
tech.root: appxpkg
ms.assetid: 0EAE15E9-5B23-43F4-B4C6-D75EC8D8F281
ms.date: 12/05/2018
ms.keywords: GetIsPackageReference, GetIsPackageReference method [App packaging and management], GetIsPackageReference method [App packaging and management],IAppxBundleManifestPackageInfo2 interface, IAppxBundleManifestPackageInfo2 interface [App packaging and management],GetIsPackageReference method, IAppxBundleManifestPackageInfo2.GetIsPackageReference, IAppxBundleManifestPackageInfo2::GetIsPackageReference, appxpackaging/IAppxBundleManifestPackageInfo2::GetIsPackageReference, appxpkg.iappxbundlemanifestpackageinfo2_getispackagereference
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
 - IAppxBundleManifestPackageInfo2::GetIsPackageReference
 - appxpackaging/IAppxBundleManifestPackageInfo2::GetIsPackageReference
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
 - IAppxBundleManifestPackageInfo2.GetIsPackageReference
---

# IAppxBundleManifestPackageInfo2::GetIsPackageReference


## -description

Determines whether a package is stored inside an app bundle, or if it's a reference to a package.

## -parameters

### -param isPackageReference [out, retval]

True if the package in the bundle is a reference to a package; False if the package in the bundle is stored inside the app bundle.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo2">IAppxBundleManifestPackageInfo2</a>