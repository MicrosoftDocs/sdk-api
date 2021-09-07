---
UID: NF:appxpackaging.IAppxManifestReader.GetDeviceCapabilities
title: IAppxManifestReader::GetDeviceCapabilities (appxpackaging.h)
description: Gets an enumerator that iterates through the device capabilities defined in the manifest.
helpviewer_keywords: ["GetDeviceCapabilities","GetDeviceCapabilities method [App packaging and management]","GetDeviceCapabilities method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetDeviceCapabilities method","IAppxManifestReader.GetDeviceCapabilities","IAppxManifestReader::GetDeviceCapabilities","appxpackaging/IAppxManifestReader::GetDeviceCapabilities","appxpkg.iappxmanifestreader_getdevicecapabilities"]
old-location: appxpkg\iappxmanifestreader_getdevicecapabilities.htm
tech.root: appxpkg
ms.assetid: 06257DB1-992E-4A8D-8221-76DA3DF0FA1F
ms.date: 12/05/2018
ms.keywords: GetDeviceCapabilities, GetDeviceCapabilities method [App packaging and management], GetDeviceCapabilities method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetDeviceCapabilities method, IAppxManifestReader.GetDeviceCapabilities, IAppxManifestReader::GetDeviceCapabilities, appxpackaging/IAppxManifestReader::GetDeviceCapabilities, appxpkg.iappxmanifestreader_getdevicecapabilities
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
 - IAppxManifestReader::GetDeviceCapabilities
 - appxpackaging/IAppxManifestReader::GetDeviceCapabilities
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
 - IAppxManifestReader.GetDeviceCapabilities
---

# IAppxManifestReader::GetDeviceCapabilities


## -description

Gets an enumerator that iterates through the device capabilities defined in the manifest.

## -parameters

### -param deviceCapabilities [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestdevicecapabilitiesenumerator">IAppxManifestDeviceCapabilitiesEnumerator</a>**</b>

The enumerator that iterates through the device capabilities.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Device capabilities are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability">DeviceCapability</a> element in the package manifest.

If no package device capabilities are defined in the manifest, this method returns <b>S_OK</b> with an empty enumerator.

Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>deviceCapabilities</i> object.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>