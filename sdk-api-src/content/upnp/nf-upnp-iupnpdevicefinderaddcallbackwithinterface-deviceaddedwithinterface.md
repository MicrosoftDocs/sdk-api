---
UID: NF:upnp.IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface
title: IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface (upnp.h)
description: The DeviceAddedWithInterface method is invoked by the UPnP framework to notify the application that a device has been added to the network.
helpviewer_keywords: ["DeviceAddedWithInterface","DeviceAddedWithInterface method [UPnP APIs]","DeviceAddedWithInterface method [UPnP APIs]","IUPnPDeviceFinderAddCallbackWithInterface interface","IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs]","DeviceAddedWithInterface method","IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface","IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface","upnp.iupnpdevicefinderaddcallbackwithinterface_deviceaddedwithinterface","upnp/IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface"]
old-location: upnp\iupnpdevicefinderaddcallbackwithinterface_deviceaddedwithinterface.htm
tech.root: upnp
ms.assetid: c7cd47e8-264b-4d1a-aed3-daf5801c240c
ms.date: 12/05/2018
ms.keywords: DeviceAddedWithInterface, DeviceAddedWithInterface method [UPnP APIs], DeviceAddedWithInterface method [UPnP APIs],IUPnPDeviceFinderAddCallbackWithInterface interface, IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs],DeviceAddedWithInterface method, IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface, IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface, upnp.iupnpdevicefinderaddcallbackwithinterface_deviceaddedwithinterface, upnp/IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface
 - upnp/IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface
---

# IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface


## -description

The <b>DeviceAddedWithInterface</b> method is invoked by the UPnP framework to notify the application that  a device has been added to the network.

## -parameters

### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>.

### -param pDevice [in]

Pointer to a <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that contains the new device.

### -param pguidInterface [in]

GUID of the network adapter through which the device advertisement came.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

The UPnP framework will query to see if the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface">IUPnPDeviceFinderAddCallbackWithInterface</a> interface exists. If you have implemented the interface, the UPnP framework will call the <b>DeviceAddedWithInterface</b> method.  Otherwise, the UPnP framework will call the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefindercallback-deviceadded">IUPnPDeviceFinderCallback::DeviceAdded</a> method.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface">IUPnPDeviceFinderAddCallbackWithInterface</a>