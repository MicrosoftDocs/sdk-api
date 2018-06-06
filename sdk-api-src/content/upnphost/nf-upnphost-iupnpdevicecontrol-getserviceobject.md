---
UID: NF:upnphost.IUPnPDeviceControl.GetServiceObject
title: IUPnPDeviceControl::GetServiceObject
author: windows-sdk-content
description: The GetServiceObject method is used to obtain the IDispatch pointer to a specific service object. The device host invokes this method once per service, the first time it receives a request for a service.
old-location: upnp\iupnpdevicecontrol_getserviceobject.htm
old-project: UPnP
ms.assetid: 55b54edf-fd1d-45b8-95d4-a746a60e5310
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: GetServiceObject, GetServiceObject method [UPnP APIs], GetServiceObject method [UPnP APIs],IUPnPDeviceControl interface, IUPnPDeviceControl interface [UPnP APIs],GetServiceObject method, IUPnPDeviceControl.GetServiceObject, IUPnPDeviceControl::GetServiceObject, _upnp_iupnpdevicecontrol_getserviceobject, upnp.iupnpdevicecontrol_getserviceobject, upnphost/IUPnPDeviceControl::GetServiceObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnphost.h
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
 - Upnphost.dll
api_name:
 - IUPnPDeviceControl.GetServiceObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceControl::GetServiceObject


## -description


The 
<b>GetServiceObject</b> method is used to obtain the <b>IDispatch</b> pointer to a specific service object. The device host invokes this method once per service, the first time it receives a request for a service.


## -parameters




### -param bstrUDN [in]

Specifies the UDN of the device.


### -param bstrServiceId [in]

Specifies the Service ID of the service for which to obtain the pointer.


### -param ppdispService






#### - pdispService [out]

Receives the <b>IDispatch</b> pointer to the service object.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -remarks



This method is invoked by the device host when a control request or event subscription is received for a particular service.

Embedded devices are differentiated by their UDNs.




## -see-also




<a href="https://msdn.microsoft.com/c5d68459-f4ba-4df1-a00c-be86e24ce29f">IUPnPDeviceControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
 

 

