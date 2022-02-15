---
UID: NN:portabledeviceapi.IPortableDeviceWebControl
title: IPortableDeviceWebControl (portabledeviceapi.h)
description: Represents a factory that can instantiate a WPD Automation Device object in a Windows Store app.
helpviewer_keywords: ["IPortableDeviceWebControl","IPortableDeviceWebControl interface [WPD Automation]","IPortableDeviceWebControl interface [WPD Automation]","described","portabledeviceapi/IPortableDeviceWebControl","wpdauto.iportabledevicewebcontrol"]
old-location: wpdauto\iportabledevicewebcontrol.htm
tech.root: wpdauto
ms.assetid: 0ec81d6a-3671-4c4e-b650-f251fa99f7ea
ms.date: 12/05/2018
ms.keywords: IPortableDeviceWebControl, IPortableDeviceWebControl interface [WPD Automation], IPortableDeviceWebControl interface [WPD Automation],described, portabledeviceapi/IPortableDeviceWebControl, wpdauto.iportabledevicewebcontrol
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [UWP apps only]
req.target-min-winversvr: Windows Server 2012 [UWP apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceapi.idl
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
 - IPortableDeviceWebControl
 - portabledeviceapi/IPortableDeviceWebControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - portabledeviceapi.h
api_name:
 - IPortableDeviceWebControl
---

# IPortableDeviceWebControl interface


## -description

Represents a factory that can instantiate a WPD Automation <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-device">Device</a> object in a Windows Store app.

## -inheritance

The <b>IPortableDeviceWebControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IPortableDeviceWebControl</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  This interface can only be used in Windows Store apps.</div>
<div> </div>

#### Examples

For WPD devices that use an MTP device service, you can create a COM Automation object to work with the device like this:


```javascript

 
deviceFactory = new ActiveXObject("PortableDeviceAutomation.Factory");
 
var device = deviceFactory.getDeviceFromId(deviceId);
// Get the first service on the device
var deviceService = device.services[0];

```

## -see-also

<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PortableDeviceServices">Portable Device Service Sample</a>
