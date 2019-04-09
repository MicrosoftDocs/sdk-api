---
UID: NF:upnp.IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface
title: IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface (upnp.h)
author: windows-sdk-content
description: The DeviceAddedWithInterface method is invoked by the UPnP framework to notify the application that a device has been added to the network.
old-location: upnp\iupnpdevicefinderaddcallbackwithinterface_deviceaddedwithinterface.htm
tech.root: upnp
ms.assetid: c7cd47e8-264b-4d1a-aed3-daf5801c240c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceAddedWithInterface, DeviceAddedWithInterface method [UPnP APIs], DeviceAddedWithInterface method [UPnP APIs],IUPnPDeviceFinderAddCallbackWithInterface interface, IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs],DeviceAddedWithInterface method, IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface, IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface, upnp.iupnpdevicefinderaddcallbackwithinterface_deviceaddedwithinterface, upnp/IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderAddCallbackWithInterface.DeviceAddedWithInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface


## -description


The <b>DeviceAddedWithInterface</b> method is invoked by the UPnP framework to notify the application that  a device has been added to the network.


## -parameters




### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>.


### -param pDevice [in]

Pointer to a <a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that contains the new device.


### -param pguidInterface [in]

GUID of the network adapter through which the device advertisement came.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



The UPnP framework will query to see if the <a href="https://msdn.microsoft.com/b0d78121-35d0-4f33-b1e9-19e0b2c5b78f">IUPnPDeviceFinderAddCallbackWithInterface</a> interface exists. If you have implemented the interface, the UPnP framework will call the <b>DeviceAddedWithInterface</b> method.  Otherwise, the UPnP framework will call the <a href="https://msdn.microsoft.com/4a61ca43-cbc6-4db2-9706-23cadbae9c3e">IUPnPDeviceFinderCallback::DeviceAdded</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/b0d78121-35d0-4f33-b1e9-19e0b2c5b78f">IUPnPDeviceFinderAddCallbackWithInterface</a>
 

 

