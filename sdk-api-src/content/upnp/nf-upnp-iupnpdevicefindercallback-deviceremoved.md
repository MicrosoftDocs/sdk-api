---
UID: NF:upnp.IUPnPDeviceFinderCallback.DeviceRemoved
title: IUPnPDeviceFinderCallback::DeviceRemoved (upnp.h)
author: windows-sdk-content
description: The DeviceRemoved method is invoked by the UPnP framework to notify the application that a device has been removed from the network.
old-location: upnp\iupnpdevicefindercallback_deviceremoved.htm
tech.root: upnp
ms.assetid: d6ff7bdd-3fdf-4ee4-84c9-e3527988fea2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceRemoved, DeviceRemoved method [UPnP APIs], DeviceRemoved method [UPnP APIs],IUPnPDeviceFinderCallback interface, IUPnPDeviceFinderCallback interface [UPnP APIs],DeviceRemoved method, IUPnPDeviceFinderCallback.DeviceRemoved, IUPnPDeviceFinderCallback::DeviceRemoved, _upnp_iupnpdevicefindercallback_deviceremoved, upnp.iupnpdevicefindercallback_deviceremoved, upnp/IUPnPDeviceFinderCallback::DeviceRemoved
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderCallback.DeviceRemoved
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceFinderCallback::DeviceRemoved


## -description


The 
<b>DeviceRemoved</b> method is invoked by the UPnP framework to notify the application that a device has been removed from the network.


## -parameters




### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>.


### -param bstrUDN [in]

Specifies the UDN of the device that was removed from the network.


## -returns



The application should return S_OK.




## -remarks



The UPnP framework might return two or more callbacks for the same device. An application can ignore subsequent device-removal callbacks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a>
 

 

