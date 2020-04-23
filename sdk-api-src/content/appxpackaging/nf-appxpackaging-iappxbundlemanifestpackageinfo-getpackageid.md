---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetPackageId
title: IAppxBundleManifestPackageInfo::GetPackageId (appxpackaging.h)
description: Retrieves an object that represents the identity of the app package.helpviewer_keywords: ["GetPackageId","GetPackageId method [App packaging and management]","GetPackageId method [App packaging and management]","IAppxBundleManifestPackageInfo interface","IAppxBundleManifestPackageInfo interface [App packaging and management]","GetPackageId method","IAppxBundleManifestPackageInfo.GetPackageId","IAppxBundleManifestPackageInfo::GetPackageId","appxpackaging/IAppxBundleManifestPackageInfo::GetPackageId","appxpkg.iappxbundlemanifestpackageinfo_getpackageid"]
old-location: appxpkg\iappxbundlemanifestpackageinfo_getpackageid.htm
tech.root: appxpkg
ms.assetid: 5C7F52C3-AB72-4023-900B-53E3B5504213
ms.date: 12/05/2018
ms.keywords: GetPackageId, GetPackageId method [App packaging and management], GetPackageId method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetPackageId method, IAppxBundleManifestPackageInfo.GetPackageId, IAppxBundleManifestPackageInfo::GetPackageId, appxpackaging/IAppxBundleManifestPackageInfo::GetPackageId, appxpkg.iappxbundlemanifestpackageinfo_getpackageid
f1_keywords:
- appxpackaging/IAppxBundleManifestPackageInfo.GetPackageId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- AppxPackaging.h
api_name:
- IAppxBundleManifestPackageInfo.GetPackageId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleManifestPackageInfo::GetPackageId


## -description


Retrieves an object that represents the identity of the app package.


## -parameters




### -param packageId [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>**</b>

The package identifier.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>packageId</i> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>
 

 

