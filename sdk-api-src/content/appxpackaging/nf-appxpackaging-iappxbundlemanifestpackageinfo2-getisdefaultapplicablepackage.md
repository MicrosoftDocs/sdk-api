---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage
title: IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage (appxpackaging.h)
description: Determines whether the app package is a default applicable package.
helpviewer_keywords: ["GetIsDefaultApplicablePackage","GetIsDefaultApplicablePackage method [App packaging and management]","GetIsDefaultApplicablePackage method [App packaging and management]","IAppxBundleManifestPackageInfo2 interface","IAppxBundleManifestPackageInfo2 interface [App packaging and management]","GetIsDefaultApplicablePackage method","IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage","IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage","appxpackaging/IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage","appxpkg.iappxbundlemanifestpackageinfo2_getisdefaultapplicablepackage"]
old-location: appxpkg\iappxbundlemanifestpackageinfo2_getisdefaultapplicablepackage.htm
tech.root: appxpkg
ms.assetid: 0C1181F5-0BD9-4F8E-A4E3-75A562ADF56A
ms.date: 12/05/2018
ms.keywords: GetIsDefaultApplicablePackage, GetIsDefaultApplicablePackage method [App packaging and management], GetIsDefaultApplicablePackage method [App packaging and management],IAppxBundleManifestPackageInfo2 interface, IAppxBundleManifestPackageInfo2 interface [App packaging and management],GetIsDefaultApplicablePackage method, IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage, IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage, appxpackaging/IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage, appxpkg.iappxbundlemanifestpackageinfo2_getisdefaultapplicablepackage
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
 - IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage
 - appxpackaging/IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage
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
 - IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage
---

# IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage


## -description

Determines whether the app package is a default applicable package.

## -parameters

### -param isDefaultApplicablePackage [out, retval]

True if the package is a default applicable package, False otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A default applicable package is a package that contains the default MRT-qualified resources. For example, a default applicable package could be English language resources that should be installed by default if no other appropriate alternative language is  available.

For more information on app resources, see <a href="/windows/uwp/app-resources/">App resources and the Resource Management System</a>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo2">IAppxBundleManifestPackageInfo2</a>