---
UID: NF:appxpackaging.IAppxManifestPackageDependency.GetName
title: IAppxManifestPackageDependency::GetName (appxpackaging.h)
description: Gets the name of the package on which the current package has a dependency.
helpviewer_keywords: ["GetName","GetName method [App packaging and management]","GetName method [App packaging and management]","IAppxManifestPackageDependency interface","IAppxManifestPackageDependency interface [App packaging and management]","GetName method","IAppxManifestPackageDependency.GetName","IAppxManifestPackageDependency::GetName","appxpackaging/IAppxManifestPackageDependency::GetName","appxpkg.iappxmanifestpackagedependency_getname"]
old-location: appxpkg\iappxmanifestpackagedependency_getname.htm
tech.root: appxpkg
ms.assetid: 0B1888D7-04E6-4684-8131-8295EF2C598B
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxManifestPackageDependency interface, IAppxManifestPackageDependency interface [App packaging and management],GetName method, IAppxManifestPackageDependency.GetName, IAppxManifestPackageDependency::GetName, appxpackaging/IAppxManifestPackageDependency::GetName, appxpkg.iappxmanifestpackagedependency_getname
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
 - IAppxManifestPackageDependency::GetName
 - appxpackaging/IAppxManifestPackageDependency::GetName
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
 - IAppxManifestPackageDependency.GetName
---

# IAppxManifestPackageDependency::GetName


## -description

Gets the name of the package on which the current package has a dependency.

## -parameters

### -param name [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The name of the package.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

The caller must free the memory allocated for <i>name</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency">IAppxManifestPackageDependency</a>