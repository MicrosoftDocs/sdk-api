---
UID: NN:appxpackaging.IAppxManifestDeviceCapabilitiesEnumerator
title: IAppxManifestDeviceCapabilitiesEnumerator (appxpackaging.h)
description: Enumerates the device capabilities defined in the package manifest.
helpviewer_keywords: ["IAppxManifestDeviceCapabilitiesEnumerator","IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management]","IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management]","described","appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator","appxpkg.iappxmanifestdevicecapabilitiesenumerator"]
old-location: appxpkg\iappxmanifestdevicecapabilitiesenumerator.htm
tech.root: appxpkg
ms.assetid: 6A544E15-BB92-48C3-963D-789B04464277
ms.date: 12/05/2018
ms.keywords: IAppxManifestDeviceCapabilitiesEnumerator, IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management], IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator, appxpkg.iappxmanifestdevicecapabilitiesenumerator
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
 - IAppxManifestDeviceCapabilitiesEnumerator
 - appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator
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
 - IAppxManifestDeviceCapabilitiesEnumerator
---

# IAppxManifestDeviceCapabilitiesEnumerator interface


## -description

Enumerates the device  capabilities defined in the package manifest.

## -inheritance

The <b>IAppxManifestDeviceCapabilitiesEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestDeviceCapabilitiesEnumerator</b> also has these types of members:

## -remarks

Device capabilities are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability">DeviceCapability</a> element in the package manifest.

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getdevicecapabilities">IAppxManifestReader::GetDeviceCapabilities</a> method.


#### Examples


```cpp
LPWSTR deviceCapability = NULL;
bool hasCurrent = false;
	
for (deviceCapabilitiesEnumerator->GetHasCurrent(&hasCurrent); hasCurrent == true;
	deviceCapabilitiesEnumerator->MoveNext(&hasCurrent))
{
	hr = deviceCapabilitiesEnumerator->GetCurrent(&deviceCapability); 

	...

	if (deviceCapability)
	{
		CoTaskMemFree(deviceCapability);
	}
}

```

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getdevicecapabilities">IAppxManifestReader::GetDeviceCapabilities</a>
