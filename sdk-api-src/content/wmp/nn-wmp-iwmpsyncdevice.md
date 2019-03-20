---
UID: NN:wmp.IWMPSyncDevice
title: IWMPSyncDevice (wmp.h)
author: windows-sdk-content
description: The IWMPSyncDevice interface represents a device to which Windows Media Player 10 or later can copy digital media files.
old-location: wmp\iwmpsyncdevice.htm
tech.root: WMP
ms.assetid: 981648e4-0cb1-4d7a-bd3b-50e1b9a7282c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSyncDevice, IWMPSyncDevice interface [Windows Media Player], IWMPSyncDevice interface [Windows Media Player],described, IWMPSyncDeviceInterface, wmp.iwmpsyncdevice, wmp/IWMPSyncDevice
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPSyncDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSyncDevice interface


## -description



The <b>IWMPSyncDevice</b> interface represents a device to which Windows Media Player 10 or later can copy digital media files. It provides methods used to specify and retrieve properties for the device and to manage the relationship between Windows Media Player and the device.

To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPSyncDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSyncDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563716(v=VS.85).aspx">createPartnership</a>
</td>
<td align="left" width="63%">
Creates a partnership between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563717(v=VS.85).aspx">deletePartnership</a>
</td>
<td align="left" width="63%">
Terminates the partnership between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563719(v=VS.85).aspx">get_connected</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the device is connected to Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563720(v=VS.85).aspx">get_deviceId</a>
</td>
<td align="left" width="63%">
Retrieves the device identifier string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563721(v=VS.85).aspx">get_deviceName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563722(v=VS.85).aspx">get_friendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the user-defined name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7f04b97-8a09-4feb-b776-649aa9d6f407">get_partnershipIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index of the device partnership.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563724(v=VS.85).aspx">get_progress</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the synchronization progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563741(v=VS.85).aspx">get_status</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the status of the relationship between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563742(v=VS.85).aspx">get_syncState</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the current synchronization state for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563718(v=VS.85).aspx">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves a metadata value from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563743(v=VS.85).aspx">isIdentical</a>
</td>
<td align="left" width="63%">
Compares the device to the specified device and retrieves a value indicating whether they are the same device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563744(v=VS.85).aspx">put_friendlyName</a>
</td>
<td align="left" width="63%">
Specifies the user defined name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563745(v=VS.85).aspx">showSettings</a>
</td>
<td align="left" width="63%">
Displays the Windows Media Player synchronization settings dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563746(v=VS.85).aspx">start</a>
</td>
<td align="left" width="63%">
Begins synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563747(v=VS.85).aspx">stop</a>
</td>
<td align="left" width="63%">
Ends synchronization.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPSyncDevice</b> by calling  <a href="https://msdn.microsoft.com/en-us/library/Dd563749(v=VS.85).aspx">IWMPSyncServices::getDevice</a>.

	


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

