---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

