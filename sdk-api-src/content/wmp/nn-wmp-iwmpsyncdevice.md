---
UID: NN:wmp.IWMPSyncDevice
title: IWMPSyncDevice
author: windows-sdk-content
description: The IWMPSyncDevice interface represents a device to which Windows Media Player 10 or later can copy digital media files.
old-location: wmp\iwmpsyncdevice.htm
old-project: WMP
ms.assetid: 981648e4-0cb1-4d7a-bd3b-50e1b9a7282c
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSyncDevice, IWMPSyncDevice interface [Windows Media Player], IWMPSyncDevice interface [Windows Media Player],described, IWMPSyncDeviceInterface, wmp.iwmpsyncdevice, wmp/IWMPSyncDevice
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPSyncDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/734a8717-3b7f-4a40-895f-b55cfabd665c">createPartnership</a>
</td>
<td align="left" width="63%">
Creates a partnership between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecb525b4-c804-47e6-8d6c-7d943010077a">deletePartnership</a>
</td>
<td align="left" width="63%">
Terminates the partnership between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c22f4247-8df9-4ac6-ad27-a0e34780b832">get_connected</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the device is connected to Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36d40dc4-5641-49dd-9ef4-31d2acd0f41d">get_deviceId</a>
</td>
<td align="left" width="63%">
Retrieves the device identifier string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daa490a9-d7b8-4162-a4e2-f88b8f091fa3">get_deviceName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72eaa17-fd7a-4844-8380-1a2547644dee">get_friendlyName</a>
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
<a href="https://msdn.microsoft.com/bc125107-0013-4c5b-aa44-9d48557d370d">get_progress</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the synchronization progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b194161-c25c-43d9-90ee-dd25ff61034b">get_status</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the status of the relationship between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c93263a1-7976-43db-b514-97d9a263a60c">get_syncState</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the current synchronization state for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a25b91b8-fe14-4fde-8b68-4e61515e0e5c">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves a metadata value from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4335d480-5af0-4764-b8f8-0e6edc1598b7">isIdentical</a>
</td>
<td align="left" width="63%">
Compares the device to the specified device and retrieves a value indicating whether they are the same device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caea8f34-8d0c-49ce-ae86-fda6c6b0b68b">put_friendlyName</a>
</td>
<td align="left" width="63%">
Specifies the user defined name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/496bb3b6-d942-4d53-8e66-5aed5f574343">showSettings</a>
</td>
<td align="left" width="63%">
Displays the Windows Media Player synchronization settings dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">start</a>
</td>
<td align="left" width="63%">
Begins synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">stop</a>
</td>
<td align="left" width="63%">
Ends synchronization.

</td>
</tr>
</table> 


Retrieve a pointer to <b>IWMPSyncDevice</b> by calling  <a href="https://msdn.microsoft.com/4c34b823-57ce-4053-9e98-308a5d4ffdef">IWMPSyncServices::getDevice</a>.

	


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

