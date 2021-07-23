---
UID: NF:appxpackaging.IAppxPackageReader.GetManifest
title: IAppxPackageReader::GetManifest (appxpackaging.h)
description: Retrieves the object model of the app manifest of the package.
helpviewer_keywords: ["GetManifest","GetManifest method [App packaging and management]","GetManifest method [App packaging and management]","IAppxPackageReader interface","IAppxPackageReader interface [App packaging and management]","GetManifest method","IAppxPackageReader.GetManifest","IAppxPackageReader::GetManifest","appxpackaging/IAppxPackageReader::GetManifest","appxpkg.iappxpackagereader_getmanifest"]
old-location: appxpkg\iappxpackagereader_getmanifest.htm
tech.root: appxpkg
ms.assetid: 5EE69CCD-C941-4346-B539-C415CE9EA1FB
ms.date: 12/05/2018
ms.keywords: GetManifest, GetManifest method [App packaging and management], GetManifest method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetManifest method, IAppxPackageReader.GetManifest, IAppxPackageReader::GetManifest, appxpackaging/IAppxPackageReader::GetManifest, appxpkg.iappxpackagereader_getmanifest
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
 - IAppxPackageReader::GetManifest
 - appxpackaging/IAppxPackageReader::GetManifest
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
 - IAppxPackageReader.GetManifest
---

# IAppxPackageReader::GetManifest


## -description

Retrieves the object model of the app manifest of the package.

## -parameters

### -param manifestReader [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>**</b>

The object model of the app manifest.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The package app manifest is validated when the package reader is created using <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>