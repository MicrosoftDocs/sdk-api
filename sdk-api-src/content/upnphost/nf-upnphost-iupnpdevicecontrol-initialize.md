---
UID: NF:upnphost.IUPnPDeviceControl.Initialize
title: IUPnPDeviceControl::Initialize
author: windows-sdk-content
description: The Initialize method is used to initialize the device. The device host invokes this method.
old-location: upnp\iupnpdevicecontrol_initialize.htm
old-project: UPnP
ms.assetid: 0c1ea343-f04b-414d-92cf-044cb117bc9c
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: IUPnPDeviceControl interface [UPnP APIs],Initialize method, IUPnPDeviceControl.Initialize, IUPnPDeviceControl::Initialize, Initialize, Initialize method [UPnP APIs], Initialize method [UPnP APIs],IUPnPDeviceControl interface, _upnp_iupnpdevicecontrol_initialize, upnp.iupnpdevicecontrol_initialize, upnphost/IUPnPDeviceControl::Initialize
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnphost.dll
api_name:
-	IUPnPDeviceControl.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceControl::Initialize


## -description


The 
<b>Initialize</b> method is used to initialize the device. The device host invokes this method.


## -parameters




### -param bstrXMLDesc [in]

Specifies the full XML device description, as published by the device host. The device description is based on the template provided by the device.


### -param bstrDeviceIdentifier [in]

Identifies the device to initialize. This is the same identifier returned by 
<a href="https://msdn.microsoft.com/1bb99a42-143b-495a-8b02-efa7ca1d4d29">IUPnPRegistrar::RegisterDevice</a> or 
<a href="https://msdn.microsoft.com/4b494b7e-4fcc-4de0-bdcc-96c68a5e0688">IUPnPRegistrar::RegisterRunningDevice</a>. It is also used to retrieve the UDN of the device using 
<a href="https://msdn.microsoft.com/dcffee59-8b2f-443c-915f-6d823018eadd">IUPnPRegistrar::GetUniqueDeviceName</a>.


### -param bstrInitString [in]

Specifies the initialization string used when this device was registered.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -remarks



This method is invoked immediately after the device control object is instantiated. It must be invoked before 
<a href="https://msdn.microsoft.com/55b54edf-fd1d-45b8-95d4-a746a60e5310">IUPnPDeviceControl::GetServiceObject</a> is invoked.

The difference between a running device and a non-running device is when the 
<b>Initialize</b> method is invoked.

For running devices, 
<b>Initialize</b> is invoked when 
<a href="https://msdn.microsoft.com/4b494b7e-4fcc-4de0-bdcc-96c68a5e0688">IUPnPRegistrar::RegisterRunningDevice</a> is invoked, and the initialization is completed before <b>IUPnPRegistrar::RegisterRunningDevice</b> returns.

For non-running devices, 
<b>Initialize</b> is not necessarily invoked when 
<a href="https://msdn.microsoft.com/1bb99a42-143b-495a-8b02-efa7ca1d4d29">IUPnPRegistrar::RegisterDevice</a> is invoked. 
<b>Initialize</b> is invoked when the first control or event request arrives.

The <i>bstrDeviceIdentifier</i> can also be used to call 
<a href="https://msdn.microsoft.com/dcffee59-8b2f-443c-915f-6d823018eadd">IUPnPRegistrar::GetUniqueDeviceName</a>.




## -see-also




<a href="https://msdn.microsoft.com/55b54edf-fd1d-45b8-95d4-a746a60e5310">GetServiceObject</a>



<a href="https://msdn.microsoft.com/c5d68459-f4ba-4df1-a00c-be86e24ce29f">IUPnPDeviceControl</a>
 

 

