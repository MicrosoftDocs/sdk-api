---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetOffset
title: IAppxBundleManifestPackageInfo::GetOffset (appxpackaging.h)
description: Retrieves the offset of the package relative to the beginning of the bundle.
helpviewer_keywords: ["GetOffset","GetOffset method [App packaging and management]","GetOffset method [App packaging and management]","IAppxBundleManifestPackageInfo interface","IAppxBundleManifestPackageInfo interface [App packaging and management]","GetOffset method","IAppxBundleManifestPackageInfo.GetOffset","IAppxBundleManifestPackageInfo::GetOffset","appxpackaging/IAppxBundleManifestPackageInfo::GetOffset","appxpkg.iappxbundlemanifestpackageinfo_getoffset"]
old-location: appxpkg\iappxbundlemanifestpackageinfo_getoffset.htm
tech.root: appxpkg
ms.assetid: A55DB4B6-2EA0-4392-B05A-FEE091913573
ms.date: 12/05/2018
ms.keywords: GetOffset, GetOffset method [App packaging and management], GetOffset method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetOffset method, IAppxBundleManifestPackageInfo.GetOffset, IAppxBundleManifestPackageInfo::GetOffset, appxpackaging/IAppxBundleManifestPackageInfo::GetOffset, appxpkg.iappxbundlemanifestpackageinfo_getoffset
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
 - IAppxBundleManifestPackageInfo::GetOffset
 - appxpackaging/IAppxBundleManifestPackageInfo::GetOffset
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
 - IAppxBundleManifestPackageInfo.GetOffset
---

# IAppxBundleManifestPackageInfo::GetOffset


## -description

Retrieves the offset of the package relative to the beginning of the bundle.

## -parameters

### -param offset [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

The offset of the package, in bytes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>