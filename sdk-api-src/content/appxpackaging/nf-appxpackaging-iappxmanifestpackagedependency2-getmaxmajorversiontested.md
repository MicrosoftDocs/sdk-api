---
UID: NF:appxpackaging.IAppxManifestPackageDependency2.GetMaxMajorVersionTested
title: IAppxManifestPackageDependency2::GetMaxMajorVersionTested (appxpackaging.h)
description: Returns the maximum major version number of the package that is tested to be compatible with the current package.
helpviewer_keywords: ["GetMaxMajorVersionTested","GetMaxMajorVersionTested method [App packaging and management]","GetMaxMajorVersionTested method [App packaging and management]","IAppxManifestPackageDependency2 interface","IAppxManifestPackageDependency2 interface [App packaging and management]","GetMaxMajorVersionTested method","IAppxManifestPackageDependency2.GetMaxMajorVersionTested","IAppxManifestPackageDependency2::GetMaxMajorVersionTested","appxpackaging/IAppxManifestPackageDependency2::GetMaxMajorVersionTested","appxpkg.iappxmanifestpackagedependency2_getmaxmajorversiontested"]
old-location: appxpkg\iappxmanifestpackagedependency2_getmaxmajorversiontested.htm
tech.root: appxpkg
ms.assetid: BB83C97E-9E89-440C-8A14-88062F1394CF
ms.date: 12/05/2018
ms.keywords: GetMaxMajorVersionTested, GetMaxMajorVersionTested method [App packaging and management], GetMaxMajorVersionTested method [App packaging and management],IAppxManifestPackageDependency2 interface, IAppxManifestPackageDependency2 interface [App packaging and management],GetMaxMajorVersionTested method, IAppxManifestPackageDependency2.GetMaxMajorVersionTested, IAppxManifestPackageDependency2::GetMaxMajorVersionTested, appxpackaging/IAppxManifestPackageDependency2::GetMaxMajorVersionTested, appxpkg.iappxmanifestpackagedependency2_getmaxmajorversiontested
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IAppxManifestPackageDependency2::GetMaxMajorVersionTested
 - appxpackaging/IAppxManifestPackageDependency2::GetMaxMajorVersionTested
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
 - IAppxManifestPackageDependency2.GetMaxMajorVersionTested
---

# IAppxManifestPackageDependency2::GetMaxMajorVersionTested


## -description

Returns the maximum major version number of  the package that is tested to be compatible
with the current package.

## -parameters

### -param maxMajorVersionTested [out]

The maximum major version number of the dependency package that has been tested to be compatible
with the current package.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 If the
<b>MaxMajorVersionTested</b> attribute is not specified for the current dependency package, this method returns the highest 16 bits of the <b>MinVersion</b> field. For more information, see the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependency-getminversion">GetMinVersion</a> method.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependency-getminversion">GetMinVersion</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency2">IAppxManifestPackageDependency2</a>