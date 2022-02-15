---
UID: NF:appxpackaging.IAppxManifestReader.GetPackageId
title: IAppxManifestReader::GetPackageId (appxpackaging.h)
description: Gets the package identifier defined in the manifest.
helpviewer_keywords: ["GetPackageId","GetPackageId method [App packaging and management]","GetPackageId method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetPackageId method","IAppxManifestReader.GetPackageId","IAppxManifestReader::GetPackageId","appxpackaging/IAppxManifestReader::GetPackageId","appxpkg.iappxmanifestreader_getpackageid"]
old-location: appxpkg\iappxmanifestreader_getpackageid.htm
tech.root: appxpkg
ms.assetid: 67E1B1A4-E934-4CCF-AF94-A7923B192A21
ms.date: 12/05/2018
ms.keywords: GetPackageId, GetPackageId method [App packaging and management], GetPackageId method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetPackageId method, IAppxManifestReader.GetPackageId, IAppxManifestReader::GetPackageId, appxpackaging/IAppxManifestReader::GetPackageId, appxpkg.iappxmanifestreader_getpackageid
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
 - IAppxManifestReader::GetPackageId
 - appxpackaging/IAppxManifestReader::GetPackageId
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
 - IAppxManifestReader.GetPackageId
---

# IAppxManifestReader::GetPackageId


## -description

Gets the package identifier defined in the manifest.

## -parameters

### -param packageId [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>**</b>

The package identifier.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>packageId</i> object.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>