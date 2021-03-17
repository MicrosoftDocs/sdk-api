---
UID: NF:upnp.IUPnPDeviceFinderCallback.DeviceAdded
title: IUPnPDeviceFinderCallback::DeviceAdded (upnp.h)
description: The DeviceAdded method is invoked by the UPnP framework to notify the application that a device has been added to the network.
helpviewer_keywords: ["DeviceAdded","DeviceAdded method [UPnP APIs]","DeviceAdded method [UPnP APIs]","IUPnPDeviceFinderCallback interface","IUPnPDeviceFinderCallback interface [UPnP APIs]","DeviceAdded method","IUPnPDeviceFinderCallback.DeviceAdded","IUPnPDeviceFinderCallback::DeviceAdded","_upnp_iupnpdevicefindercallback_deviceadded","upnp.iupnpdevicefindercallback_deviceadded","upnp/IUPnPDeviceFinderCallback::DeviceAdded"]
old-location: upnp\iupnpdevicefindercallback_deviceadded.htm
tech.root: upnp
ms.assetid: 4a61ca43-cbc6-4db2-9706-23cadbae9c3e
ms.date: 12/05/2018
ms.keywords: DeviceAdded, DeviceAdded method [UPnP APIs], DeviceAdded method [UPnP APIs],IUPnPDeviceFinderCallback interface, IUPnPDeviceFinderCallback interface [UPnP APIs],DeviceAdded method, IUPnPDeviceFinderCallback.DeviceAdded, IUPnPDeviceFinderCallback::DeviceAdded, _upnp_iupnpdevicefindercallback_deviceadded, upnp.iupnpdevicefindercallback_deviceadded, upnp/IUPnPDeviceFinderCallback::DeviceAdded
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IUPnPDeviceFinderCallback::DeviceAdded
 - upnp/IUPnPDeviceFinderCallback::DeviceAdded
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
 - IUPnPDeviceFinderCallback.DeviceAdded
---

# IUPnPDeviceFinderCallback::DeviceAdded


## -description

The 
<b>DeviceAdded</b> method is invoked by the UPnP framework to notify the application that a device has been added to the network.

## -parameters

### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>.

### -param pDevice [in]

Reference to a 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that contains the new device.

## -returns

The UPnP framework does not expect the application to return any specific value; any value returned is ignored by the UPnP framework.

## -remarks

The UPnP framework might call the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinderaddcallbackwithinterface-deviceaddedwithinterface">IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface</a> method instead of <b>DeviceAdded</b> to notify the application when a device is added to the network. The UPnP framework will query to see if the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface">IUPnPDeviceFinderAddCallbackWithInterface</a> interface exists. If so, the UPnP framework will call <b>DeviceAddedWithInterface</b>.  Otherwise, the UPnP framework will call <b>DeviceAdded</b>.

The UPnP framework might return two or more callbacks for the same device. This can happen if a device's IP address was changed without first removing the device, and then re-adding it to the network. If this occurs, an application should discard the old device and use the most recently returned one. An application checks for duplicate devices by comparing the UDNs.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a>