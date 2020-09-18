---
UID: NF:appxpackaging.IAppxManifestPackageId.GetName
title: IAppxManifestPackageId::GetName (appxpackaging.h)
description: Gets the name of the package as defined in the manifest.
helpviewer_keywords: ["GetName","GetName method [App packaging and management]","GetName method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","GetName method","IAppxManifestPackageId.GetName","IAppxManifestPackageId::GetName","appxpackaging/IAppxManifestPackageId::GetName","appxpkg.iappxmanifestpackageid_getname"]
old-location: appxpkg\iappxmanifestpackageid_getname.htm
tech.root: appxpkg
ms.assetid: F59FDC61-BA78-4204-AAD3-C34B7F1EB37B
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetName method, IAppxManifestPackageId.GetName, IAppxManifestPackageId::GetName, appxpackaging/IAppxManifestPackageId::GetName, appxpkg.iappxmanifestpackageid_getname
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
 - IAppxManifestPackageId::GetName
 - appxpackaging/IAppxManifestPackageId::GetName
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
 - IAppxManifestPackageId.GetName
---

# IAppxManifestPackageId::GetName


## -description

Gets the name of the package as defined in the manifest.

## -parameters

### -param name [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The name of the package.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

Package name information is specified using the <b>Name</b> attribute of the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity">Identity</a> element in the package manifest.

The package name is not intended to be displayed to end users. Rather, the system uses it to uniquely identify the package.

The caller must free the memory allocated for <i>name</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>