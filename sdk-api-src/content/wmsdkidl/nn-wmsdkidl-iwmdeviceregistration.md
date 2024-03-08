---
UID: NN:wmsdkidl.IWMDeviceRegistration
title: IWMDeviceRegistration (wmsdkidl.h)
description: The IWMDeviceRegistration interface registers playback devices for secure data delivery.You can create a device registration object and retrieve a pointer to its IWMDeviceRegistration interface by calling the WMCreateDeviceRegistration function.
helpviewer_keywords: ["IWMDeviceRegistration","IWMDeviceRegistration interface [windows Media Format]","IWMDeviceRegistration interface [windows Media Format]","described","IWMDeviceRegistrationInterface","wmformat.iwmdeviceregistration","wmsdkidl/IWMDeviceRegistration"]
old-location: wmformat\iwmdeviceregistration.htm
tech.root: wmformat
ms.assetid: fb08ddae-2abf-4a86-a5d8-ea745ae35aa8
ms.date: 4/26/2023
ms.keywords: IWMDeviceRegistration, IWMDeviceRegistration interface [windows Media Format], IWMDeviceRegistration interface [windows Media Format],described, IWMDeviceRegistrationInterface, wmformat.iwmdeviceregistration, wmsdkidl/IWMDeviceRegistration
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
 - IWMDeviceRegistration
 - wmsdkidl/IWMDeviceRegistration
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
 - IWMDeviceRegistration
---

# IWMDeviceRegistration interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMDeviceRegistration</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDeviceRegistration</b> interface registers playback devices for secure data delivery.

You can create a device registration object and retrieve a pointer to its <b>IWMDeviceRegistration</b> interface by calling the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration">WMCreateDeviceRegistration</a> function.

## -inheritance

The <b>IWMDeviceRegistration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDeviceRegistration</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The primary purpose of the device registration database is to store data about connected devices that can receive streaming media encoded for the Windows Media DRM 10 for Network Devices protocol. You can enter other devices in the database if desired.

The device registration database is a secure database on the client computer. All interactions with the database are managed internally; your application does not have direct access to it.

The same device registration database is used by all applications.

Devices in the database are registered by type. Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type. Other types may be supported in future versions.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
