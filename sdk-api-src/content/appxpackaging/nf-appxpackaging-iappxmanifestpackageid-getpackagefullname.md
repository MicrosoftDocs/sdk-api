---
UID: NF:appxpackaging.IAppxManifestPackageId.GetPackageFullName
title: IAppxManifestPackageId::GetPackageFullName (appxpackaging.h)
description: Gets the package full name.
helpviewer_keywords: ["GetPackageFullName","GetPackageFullName method [App packaging and management]","GetPackageFullName method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","GetPackageFullName method","IAppxManifestPackageId.GetPackageFullName","IAppxManifestPackageId::GetPackageFullName","appxpackaging/IAppxManifestPackageId::GetPackageFullName","appxpkg.iappxmanifestpackageid_getpackagefullname"]
old-location: appxpkg\iappxmanifestpackageid_getpackagefullname.htm
tech.root: appxpkg
ms.assetid: 514D2E04-5CA5-4F45-A6D8-96866588EECF
ms.date: 12/05/2018
ms.keywords: GetPackageFullName, GetPackageFullName method [App packaging and management], GetPackageFullName method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetPackageFullName method, IAppxManifestPackageId.GetPackageFullName, IAppxManifestPackageId::GetPackageFullName, appxpackaging/IAppxManifestPackageId::GetPackageFullName, appxpkg.iappxmanifestpackageid_getpackagefullname
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
 - IAppxManifestPackageId::GetPackageFullName
 - appxpackaging/IAppxManifestPackageId::GetPackageFullName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernelbase.dll
api_name:
 - IAppxManifestPackageId.GetPackageFullName
---

# IAppxManifestPackageId::GetPackageFullName


## -description

Gets the package full name.

## -parameters

### -param packageFullName [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The package full name.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

The package full name string is a case-insensitive string, which can be used to uniquely identify the package. 

This string  is a serialized form of the package ID, and it is suitable for naming objects such as files and directories.

The caller must free the memory allocated for <i>packageFullName</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>