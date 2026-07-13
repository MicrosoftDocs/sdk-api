---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo2.GetIsNonQualifiedResourcePackage
title: IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage (appxpackaging.h)
description: Determines whether the app package is a non-qualified resource package.
helpviewer_keywords: ["GetIsNonQualifiedResourcePackage","GetIsNonQualifiedResourcePackage method [App packaging and management]","GetIsNonQualifiedResourcePackage method [App packaging and management]","IAppxBundleManifestPackageInfo2 interface","IAppxBundleManifestPackageInfo2 interface [App packaging and management]","GetIsNonQualifiedResourcePackage method","IAppxBundleManifestPackageInfo2.GetIsNonQualifiedResourcePackage","IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage","appxpackaging/IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage","appxpkg.iappxbundlemanifestpackageinfo2_getisnonqualifiedresourcepackage"]
old-location: appxpkg\iappxbundlemanifestpackageinfo2_getisnonqualifiedresourcepackage.htm
tech.root: appxpkg
ms.assetid: C6AA5EE3-DE41-41DD-8804-70CDCA817C7A
ms.date: 12/05/2018
ms.keywords: GetIsNonQualifiedResourcePackage, GetIsNonQualifiedResourcePackage method [App packaging and management], GetIsNonQualifiedResourcePackage method [App packaging and management],IAppxBundleManifestPackageInfo2 interface, IAppxBundleManifestPackageInfo2 interface [App packaging and management],GetIsNonQualifiedResourcePackage method, IAppxBundleManifestPackageInfo2.GetIsNonQualifiedResourcePackage, IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage, appxpackaging/IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage, appxpkg.iappxbundlemanifestpackageinfo2_getisnonqualifiedresourcepackage
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
 - IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage
 - appxpackaging/IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage
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
 - IAppxBundleManifestPackageInfo2.GetIsNonQualifiedResourcePackage
---

# IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage


## -description

Determines whether the app package is a non-qualified resource package.

## -parameters

### -param isNonQualifiedResourcePackage [out, retval]

True if the package is a non-qualified resource package, False otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A non-qualified resource package is a package that contains resources that are not qualified with any language, scale, or other qualifier. An example of this could be a package that contains all music files. 

For more information on app resources, see <a href="/windows/uwp/app-resources/">App resources and the Resource Management System</a>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo2">IAppxBundleManifestPackageInfo2</a>