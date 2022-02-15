---
UID: NF:appxpackaging.IAppxManifestPackageDependency.GetMinVersion
title: IAppxManifestPackageDependency::GetMinVersion (appxpackaging.h)
description: Gets the minimum version of the package on which the current package has a dependency.
helpviewer_keywords: ["GetMinVersion","GetMinVersion method [App packaging and management]","GetMinVersion method [App packaging and management]","IAppxManifestPackageDependency interface","IAppxManifestPackageDependency interface [App packaging and management]","GetMinVersion method","IAppxManifestPackageDependency.GetMinVersion","IAppxManifestPackageDependency::GetMinVersion","appxpackaging/IAppxManifestPackageDependency::GetMinVersion","appxpkg.iappxmanifestpackagedependency_getminversion"]
old-location: appxpkg\iappxmanifestpackagedependency_getminversion.htm
tech.root: appxpkg
ms.assetid: 301053BA-A2DB-405C-9E2E-3817B2B5D7FD
ms.date: 12/05/2018
ms.keywords: GetMinVersion, GetMinVersion method [App packaging and management], GetMinVersion method [App packaging and management],IAppxManifestPackageDependency interface, IAppxManifestPackageDependency interface [App packaging and management],GetMinVersion method, IAppxManifestPackageDependency.GetMinVersion, IAppxManifestPackageDependency::GetMinVersion, appxpackaging/IAppxManifestPackageDependency::GetMinVersion, appxpkg.iappxmanifestpackagedependency_getminversion
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
 - IAppxManifestPackageDependency::GetMinVersion
 - appxpackaging/IAppxManifestPackageDependency::GetMinVersion
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
 - IAppxManifestPackageDependency.GetMinVersion
---

# IAppxManifestPackageDependency::GetMinVersion


## -description

Gets the minimum version of the package on which the current package has a dependency.

## -parameters

### -param minVersion [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

The minimum version of the package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the minimum version is not defined for the dependency, this method returns <b>S_OK</b> and <i>minVersion</i> is 0.

The version is specified using the <b>MinVersion</b> attribute of the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-packagedependency">PackageDependency</a> element in the package manifest. The specification in the manifest is in quad notation:

<i>major</i>.<i>minor</i>.<i>build</i>.<i>revision</i>

This method converts this notation to a <b>UINT64</b> value as follows:

<ul>
<li>The high-order word contains the major version</li>
<li>The next word contains the minor version</li>
<li>The next word contains the build number</li>
<li>The low-order word contains the revision</li>
</ul>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency">IAppxManifestPackageDependency</a>