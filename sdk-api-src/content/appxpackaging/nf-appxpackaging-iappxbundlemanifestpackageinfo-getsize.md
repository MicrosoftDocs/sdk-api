---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetSize
title: IAppxBundleManifestPackageInfo::GetSize (appxpackaging.h)
description: Retrieves the size of the package, in bytes.
helpviewer_keywords: ["GetSize","GetSize method [App packaging and management]","GetSize method [App packaging and management]","IAppxBundleManifestPackageInfo interface","IAppxBundleManifestPackageInfo interface [App packaging and management]","GetSize method","IAppxBundleManifestPackageInfo.GetSize","IAppxBundleManifestPackageInfo::GetSize","appxpackaging/IAppxBundleManifestPackageInfo::GetSize","appxpkg.iappxbundlemanifestpackageinfo_getsize"]
old-location: appxpkg\iappxbundlemanifestpackageinfo_getsize.htm
tech.root: appxpkg
ms.assetid: BA9BB378-D9AF-4D96-88B0-219A5545397A
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [App packaging and management], GetSize method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetSize method, IAppxBundleManifestPackageInfo.GetSize, IAppxBundleManifestPackageInfo::GetSize, appxpackaging/IAppxBundleManifestPackageInfo::GetSize, appxpkg.iappxbundlemanifestpackageinfo_getsize
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
 - IAppxBundleManifestPackageInfo::GetSize
 - appxpackaging/IAppxBundleManifestPackageInfo::GetSize
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
 - IAppxBundleManifestPackageInfo.GetSize
---

# IAppxBundleManifestPackageInfo::GetSize


## -description

Retrieves the size of the package, in bytes.

## -parameters

### -param size [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

The size of the package, in bytes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>