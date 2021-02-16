---
UID: NF:appxpackaging.IAppxManifestPackageId.GetPackageFamilyName
title: IAppxManifestPackageId::GetPackageFamilyName (appxpackaging.h)
description: Gets the package family name.
helpviewer_keywords: ["GetPackageFamilyName","GetPackageFamilyName method [App packaging and management]","GetPackageFamilyName method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","GetPackageFamilyName method","IAppxManifestPackageId.GetPackageFamilyName","IAppxManifestPackageId::GetPackageFamilyName","appxpackaging/IAppxManifestPackageId::GetPackageFamilyName","appxpkg.iappxmanifestpackageid_getpackagefamilyname"]
old-location: appxpkg\iappxmanifestpackageid_getpackagefamilyname.htm
tech.root: appxpkg
ms.assetid: A4505020-61CB-4893-AB3B-6EF0E55FD225
ms.date: 12/05/2018
ms.keywords: GetPackageFamilyName, GetPackageFamilyName method [App packaging and management], GetPackageFamilyName method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetPackageFamilyName method, IAppxManifestPackageId.GetPackageFamilyName, IAppxManifestPackageId::GetPackageFamilyName, appxpackaging/IAppxManifestPackageId::GetPackageFamilyName, appxpkg.iappxmanifestpackageid_getpackagefamilyname
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
 - IAppxManifestPackageId::GetPackageFamilyName
 - appxpackaging/IAppxManifestPackageId::GetPackageFamilyName
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
 - IAppxManifestPackageId.GetPackageFamilyName
---

# IAppxManifestPackageId::GetPackageFamilyName


## -description

Gets the package family name.

## -parameters

### -param packageFamilyName [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The package family name.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

The package family name is a case-insensitive string, which can be used to uniquely identify a family of packages with the same name and publisher. 

This string is a serialized form of the package ID, and it is suitable for naming objects such as files and directories. Because the package family name does not contain information about package version, architecture, or resources, it is useful when you need a version-independent reference to a package.

The caller must free the memory for <i>packageFamilyName</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>