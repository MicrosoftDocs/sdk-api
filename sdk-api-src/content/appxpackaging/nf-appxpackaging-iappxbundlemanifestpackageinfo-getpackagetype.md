---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetPackageType
title: IAppxBundleManifestPackageInfo::GetPackageType (appxpackaging.h)
description: Retrieves the type of package that is represented by the package info.
helpviewer_keywords: ["GetPackageType","GetPackageType method [App packaging and management]","GetPackageType method [App packaging and management]","IAppxBundleManifestPackageInfo interface","IAppxBundleManifestPackageInfo interface [App packaging and management]","GetPackageType method","IAppxBundleManifestPackageInfo.GetPackageType","IAppxBundleManifestPackageInfo::GetPackageType","appxpackaging/IAppxBundleManifestPackageInfo::GetPackageType","appxpkg.iappxbundlemanifestpackageinfo_getpackagetype"]
old-location: appxpkg\iappxbundlemanifestpackageinfo_getpackagetype.htm
tech.root: appxpkg
ms.assetid: 965E48E3-7C60-4299-85F4-07CB879E7B39
ms.date: 12/05/2018
ms.keywords: GetPackageType, GetPackageType method [App packaging and management], GetPackageType method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetPackageType method, IAppxBundleManifestPackageInfo.GetPackageType, IAppxBundleManifestPackageInfo::GetPackageType, appxpackaging/IAppxBundleManifestPackageInfo::GetPackageType, appxpkg.iappxbundlemanifestpackageinfo_getpackagetype
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleManifestPackageInfo::GetPackageType
 - appxpackaging/IAppxBundleManifestPackageInfo::GetPackageType
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
 - IAppxBundleManifestPackageInfo.GetPackageType
---

# IAppxBundleManifestPackageInfo::GetPackageType


## -description

Retrieves the type of package that is represented by the package info.

## -parameters

### -param packageType [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_bundle_payload_package_type">APPX_BUNDLE_PAYLOAD_PACKAGE_TYPE</a>*</b>

The type of package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>