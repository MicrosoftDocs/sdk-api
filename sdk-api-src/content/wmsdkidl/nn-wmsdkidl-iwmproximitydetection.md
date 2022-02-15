---
UID: NN:wmsdkidl.IWMProximityDetection
title: IWMProximityDetection (wmsdkidl.h)
description: The IWMProximityDetection interface validates a playback device for receiving media data.
helpviewer_keywords: ["IWMProximityDetection","IWMProximityDetection interface [windows Media Format]","IWMProximityDetection interface [windows Media Format]","described","IWMProximityDetectionInterface","wmformat.iwmproximitydetection","wmsdkidl/IWMProximityDetection"]
old-location: wmformat\iwmproximitydetection.htm
tech.root: wmformat
ms.assetid: 0897ad8f-8e06-4de9-840e-1588e0e20c54
ms.date: 12/05/2018
ms.keywords: IWMProximityDetection, IWMProximityDetection interface [windows Media Format], IWMProximityDetection interface [windows Media Format],described, IWMProximityDetectionInterface, wmformat.iwmproximitydetection, wmsdkidl/IWMProximityDetection
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IWMProximityDetection
 - wmsdkidl/IWMProximityDetection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMProximityDetection
---

# IWMProximityDetection interface


## -description

<p class="CCE_Message">[<b>IWMProximityDetection</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMProximityDetection</b> interface validates a playback device for receiving media data. The validation process confirms that the device is "near" enough on the network to receive media through the Windows Media DRM 10 for Network Devices protocol.

An <b>IWMProximityDetection</b> interface exists for every device registration object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration</a> interface.

## -inheritance

The <b>IWMProximityDetection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMProximityDetection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

The validation state is stored in the device registration database. You can check the validation state for a device by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid">IWMRegisteredDevice::IsValid</a>.

Validation expires after 48 hours.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
