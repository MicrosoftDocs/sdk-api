---
UID: NF:appxpackaging.IAppxManifestReader.GetProperties
title: IAppxManifestReader::GetProperties (appxpackaging.h)
description: Gets the properties of the package as defined in the manifest.
helpviewer_keywords: ["GetProperties","GetProperties method [App packaging and management]","GetProperties method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetProperties method","IAppxManifestReader.GetProperties","IAppxManifestReader::GetProperties","appxpackaging/IAppxManifestReader::GetProperties","appxpkg.iappxmanifestreader_getproperties"]
old-location: appxpkg\iappxmanifestreader_getproperties.htm
tech.root: appxpkg
ms.assetid: E507BA9D-D2CA-4B28-BD13-B820B666B4C6
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [App packaging and management], GetProperties method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetProperties method, IAppxManifestReader.GetProperties, IAppxManifestReader::GetProperties, appxpackaging/IAppxManifestReader::GetProperties, appxpkg.iappxmanifestreader_getproperties
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
 - IAppxManifestReader::GetProperties
 - appxpackaging/IAppxManifestReader::GetProperties
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
 - IAppxManifestReader.GetProperties
---

# IAppxManifestReader::GetProperties


## -description

Gets the properties of the package as defined in the manifest.

## -parameters

### -param packageProperties [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestproperties">IAppxManifestProperties</a>**</b>

Properties of the package as described by the manifest.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

Properties are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-properties">Properties</a> element in the manifest.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>