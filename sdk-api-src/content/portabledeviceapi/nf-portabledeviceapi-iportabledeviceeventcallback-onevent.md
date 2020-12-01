---
UID: NF:portabledeviceapi.IPortableDeviceEventCallback.OnEvent
title: IPortableDeviceEventCallback::OnEvent (portabledeviceapi.h)
description: The OnEvent method is called by the SDK to notify the application about asynchronous events.
helpviewer_keywords: ["IPortableDeviceEventCallback interface [Windows Portable Devices SDK]","OnEvent method","IPortableDeviceEventCallback.OnEvent","IPortableDeviceEventCallback::OnEvent","IPortableDeviceEventCallbackOnEvent","OnEvent","OnEvent method [Windows Portable Devices SDK]","OnEvent method [Windows Portable Devices SDK]","IPortableDeviceEventCallback interface","portabledeviceapi/IPortableDeviceEventCallback::OnEvent","wpdsdk.iportabledeviceeventcallback_onevent"]
old-location: wpdsdk\iportabledeviceeventcallback_onevent.htm
tech.root: wpdsdk
ms.assetid: 14659de0-5cea-458a-bf57-fe8b071c778a
ms.date: 12/05/2018
ms.keywords: IPortableDeviceEventCallback interface [Windows Portable Devices SDK],OnEvent method, IPortableDeviceEventCallback.OnEvent, IPortableDeviceEventCallback::OnEvent, IPortableDeviceEventCallbackOnEvent, OnEvent, OnEvent method [Windows Portable Devices SDK], OnEvent method [Windows Portable Devices SDK],IPortableDeviceEventCallback interface, portabledeviceapi/IPortableDeviceEventCallback::OnEvent, wpdsdk.iportabledeviceeventcallback_onevent
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceEventCallback::OnEvent
 - portabledeviceapi/IPortableDeviceEventCallback::OnEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceEventCallback.OnEvent
---

# IPortableDeviceEventCallback::OnEvent


## -description

The <b>OnEvent</b> method is called by the SDK to notify the application about asynchronous events.

## -parameters

### -param pEventParameters [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains event details.

## -returns

Any values returned by the application are ignored by Windows Portable Devices.

## -remarks

The application must register to receive events by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-advise">IPortableDevice::Advise</a>.


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/handling-events-from-the-device">Handling Events from the Device</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/wpd_sdk/handling-events-from-the-device">Handling Events from the Device</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceeventcallback">IPortableDeviceEventCallback Interface</a>