---
UID: NN:portabledeviceapi.IPortableDeviceWebControl
title: IPortableDeviceWebControl
author: windows-driver-content
description: Represents a factory that can instantiate a WPD Automation Device object in a Windows Store app.
old-location: wpdauto\iportabledevicewebcontrol.htm
old-project: wpdauto
ms.assetid: 0ec81d6a-3671-4c4e-b650-f251fa99f7ea
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IPortableDeviceWebControl, IPortableDeviceWebControl interface [WPD Automation], IPortableDeviceWebControl interface [WPD Automation],described, portabledeviceapi/IPortableDeviceWebControl, wpdauto.iportabledevicewebcontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	portabledeviceapi.h
api_name:
-	IPortableDeviceWebControl
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceWebControl interface


## -description


Represents a factory that can instantiate a WPD Automation <a href="wpdauto.device_object_script">Device</a> object in a Windows Store app.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceWebControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IPortableDeviceWebControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceWebControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba375082-3f4f-44d7-96d3-bf8151408b9e">GetDeviceFromId</a>
</td>
<td align="left" width="63%">
Instantiates a WPD Automation <a href="wpdauto.device_object_script">Device</a> object for a given WPD device identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a53e4a15-4f51-43e7-84c7-4c75be87e3d9">GetDeviceFromIdAsync</a>
</td>
<td align="left" width="63%">
Instantiates a WPD Automation <a href="wpdauto.device_object_script">Device</a> object asynchronously for a given WPD device identifier.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  This interface can only be used in Windows Store apps.</div>
<div> </div>

#### Examples

For WPD devices that use an MTP device service, you can create a COM Automation object to work with the device like this:

<div class="code"><span codelanguage="JavaScript"><table>
<tr>
<th>JavaScript</th>
</tr>
<tr>
<td>
<pre>
 
deviceFactory = new ActiveXObject("PortableDeviceAutomation.Factory");
 
var device = deviceFactory.getDeviceFromId(deviceId);
// Get the first service on the device
var deviceService = device.services[0];
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=266421">Portable Device Service Sample</a>
 

 

