---
UID: NF:upnp.IUPnPDeviceFinderCallback.DeviceAdded
title: IUPnPDeviceFinderCallback::DeviceAdded
author: windows-sdk-content
description: The DeviceAdded method is invoked by the UPnP framework to notify the application that a device has been added to the network.
old-location: upnp\iupnpdevicefindercallback_deviceadded.htm
old-project: upnp
ms.assetid: 4a61ca43-cbc6-4db2-9706-23cadbae9c3e
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DeviceAdded, DeviceAdded method [UPnP APIs], DeviceAdded method [UPnP APIs],IUPnPDeviceFinderCallback interface, IUPnPDeviceFinderCallback interface [UPnP APIs],DeviceAdded method, IUPnPDeviceFinderCallback.DeviceAdded, IUPnPDeviceFinderCallback::DeviceAdded, _upnp_iupnpdevicefindercallback_deviceadded, upnp.iupnpdevicefindercallback_deviceadded, upnp/IUPnPDeviceFinderCallback::DeviceAdded
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderCallback.DeviceAdded
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceFinderCallback::DeviceAdded


## -description


The 
<b>DeviceAdded</b> method is invoked by the UPnP framework to notify the application that a device has been added to the network.


## -parameters




### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>.


### -param pDevice [in]

Reference to a 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that contains the new device.


## -returns



The UPnP framework does not expect the application to return any specific value; any value returned is ignored by the UPnP framework.




## -remarks



The UPnP framework might call the <a href="https://msdn.microsoft.com/c7cd47e8-264b-4d1a-aed3-daf5801c240c">IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface</a> method instead of <b>DeviceAdded</b> to notify the application when a device is added to the network. The UPnP framework will query to see if the <a href="https://msdn.microsoft.com/b0d78121-35d0-4f33-b1e9-19e0b2c5b78f">IUPnPDeviceFinderAddCallbackWithInterface</a> interface exists. If so, the UPnP framework will call <b>DeviceAddedWithInterface</b>.  Otherwise, the UPnP framework will call <b>DeviceAdded</b>.

The UPnP framework might return two or more callbacks for the same device. This can happen if a device's IP address was changed without first removing the device, and then re-adding it to the network. If this occurs, an application should discard the old device and use the most recently returned one. An application checks for duplicate devices by comparing the UDNs.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="https://msdn.microsoft.com/02f1220b-d400-469e-8a28-64871f7fcbe2">IUPnPDeviceFinderCallback</a>
 

 

