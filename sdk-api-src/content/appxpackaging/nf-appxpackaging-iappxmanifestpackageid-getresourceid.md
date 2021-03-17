---
UID: NF:appxpackaging.IAppxManifestPackageId.GetResourceId
title: IAppxManifestPackageId::GetResourceId (appxpackaging.h)
description: Gets the package resource identifier as defined in the manifest.
helpviewer_keywords: ["GetResourceId","GetResourceId method [App packaging and management]","GetResourceId method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","GetResourceId method","IAppxManifestPackageId.GetResourceId","IAppxManifestPackageId::GetResourceId","appxpackaging/IAppxManifestPackageId::GetResourceId","appxpkg.iappxmanifestpackageid_getresourceid"]
old-location: appxpkg\iappxmanifestpackageid_getresourceid.htm
tech.root: appxpkg
ms.assetid: D17BD71A-6418-4229-8829-2C8EB9393285
ms.date: 12/05/2018
ms.keywords: GetResourceId, GetResourceId method [App packaging and management], GetResourceId method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetResourceId method, IAppxManifestPackageId.GetResourceId, IAppxManifestPackageId::GetResourceId, appxpackaging/IAppxManifestPackageId::GetResourceId, appxpkg.iappxmanifestpackageid_getresourceid
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
 - IAppxManifestPackageId::GetResourceId
 - appxpackaging/IAppxManifestPackageId::GetResourceId
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
 - IAppxManifestPackageId.GetResourceId
---

# IAppxManifestPackageId::GetResourceId


## -description

Gets the package resource identifier as defined in the manifest.

## -parameters

### -param resourceId [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The resource identifier of the package.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

The resource identifier is specified using the <b>ResourceId</b> attribute of the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity">Identity</a> element in the package manifest.

If no resource identifier is defined in the manifest, this method returns a null string.

The caller must free the memory allocated for <i>resourceId</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>