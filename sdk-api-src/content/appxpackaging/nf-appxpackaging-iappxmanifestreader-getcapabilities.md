---
UID: NF:appxpackaging.IAppxManifestReader.GetCapabilities
title: IAppxManifestReader::GetCapabilities (appxpackaging.h)
description: Gets the list of capabilities requested by the package.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [App packaging and management]","GetCapabilities method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetCapabilities method","IAppxManifestReader.GetCapabilities","IAppxManifestReader::GetCapabilities","appxpackaging/IAppxManifestReader::GetCapabilities","appxpkg.iappxmanifestreader_getcapabilities"]
old-location: appxpkg\iappxmanifestreader_getcapabilities.htm
tech.root: appxpkg
ms.assetid: 5FCBD9E9-9A5E-49E1-8B80-8F84EDA8B07C
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [App packaging and management], GetCapabilities method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetCapabilities method, IAppxManifestReader.GetCapabilities, IAppxManifestReader::GetCapabilities, appxpackaging/IAppxManifestReader::GetCapabilities, appxpkg.iappxmanifestreader_getcapabilities
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
 - IAppxManifestReader::GetCapabilities
 - appxpackaging/IAppxManifestReader::GetCapabilities
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
 - IAppxManifestReader.GetCapabilities
---

# IAppxManifestReader::GetCapabilities


## -description

Gets the list of capabilities requested by the package.

## -parameters

### -param capabilities [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_capabilities">APPX_CAPABILITIES</a>*</b>

The list of capabilities requested by the package. This is a bitwise combination of  the values of the enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Capabilities are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-capability">Capability</a> element in the package manifest.

If no package capabilities are defined in the manifest, this method returns <b>S_OK</b> with a zero value.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>