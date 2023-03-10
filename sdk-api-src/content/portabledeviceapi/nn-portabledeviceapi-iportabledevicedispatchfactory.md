---
UID: NN:portabledeviceapi.IPortableDeviceDispatchFactory
title: IPortableDeviceDispatchFactory (portabledeviceapi.h)
description: Represents a factory that can instantiate a WPD Automation Device object.
helpviewer_keywords: ["IPortableDeviceDispatchFactory","IPortableDeviceDispatchFactory interface [WPD Automation]","IPortableDeviceDispatchFactory interface [WPD Automation]","described","portabledeviceapi/IPortableDeviceDispatchFactory","wpdauto.iportabledevicedispatchfactory_interface"]
old-location: wpdauto\iportabledevicedispatchfactory_interface.htm
tech.root: wpdauto
ms.assetid: 537551c9-0773-44a9-b602-7d2a6bf9ad00
ms.date: 12/05/2018
ms.keywords: IPortableDeviceDispatchFactory, IPortableDeviceDispatchFactory interface [WPD Automation], IPortableDeviceDispatchFactory interface [WPD Automation],described, portabledeviceapi/IPortableDeviceDispatchFactory, wpdauto.iportabledevicedispatchfactory_interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceDispatchFactory
 - portabledeviceapi/IPortableDeviceDispatchFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceDispatchFactory
---

# IPortableDeviceDispatchFactory interface


## -description

Represents a factory that can instantiate a WPD Automation <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-device">Device</a> object.

## -inheritance

The <b>IPortableDeviceDispatchFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceDispatchFactory</b> also has these types of members:

## -remarks

The <b>IPortableDeviceDispatchFactory</b> interface can be CoCreated directly using <b>CLSID_PortableDeviceDispatchFactory</b> as in the following code.


```cpp
IPortableDeviceDispatchFactgory* pDeviceDispatchFactory = NULL;
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceDispatchFactory, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDeviceDispatchFactory));   

```



#### Examples

For an example of how to use the <b>IPortableDeviceDispatchFactory</b> interface to instantiate a WPD Automation <b>Device</b>  object, see 
  <a href="/previous-versions/windows/desktop/wpdauto/instantiating-the-wpd-automation-factory-interface">Instantiating the WPD Automation Factory Interface</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd389207(v=vs.85)">Device Object</a>



<a href="/previous-versions/windows/desktop/wpdauto/instantiating-the-wpd-automation-factory-interface">Instantiating the WPD Automation Factory Interface</a>



<a href="/previous-versions/windows/desktop/wpdauto/wpd-automation-reference">WPD Automation Reference</a>
