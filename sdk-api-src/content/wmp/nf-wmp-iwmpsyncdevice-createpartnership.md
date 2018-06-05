---
UID: NF:wmp.IWMPSyncDevice.createPartnership
title: IWMPSyncDevice::createPartnership
author: windows-sdk-content
description: The createPartnership method creates a partnership between Windows Media Player and the device.
old-location: wmp\iwmpsyncdevice_createpartnership.htm
old-project: WMP
ms.assetid: 734a8717-3b7f-4a40-895f-b55cfabd665c
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],createPartnership method, IWMPSyncDevice.createPartnership, IWMPSyncDevice::createPartnership, IWMPSyncDevicecreatePartnership, createPartnership, createPartnership method [Windows Media Player], createPartnership method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_createpartnership, wmp/IWMPSyncDevice::createPartnership
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSyncDevice.createPartnership
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSyncDevice::createPartnership


## -description



The <b>createPartnership</b> method creates a partnership between Windows Media Player and the device.




## -parameters




### -param vbShowUI [out]

<b>VARIANT_BOOL</b> that specifies whether Windows Media Player displays the <b>Device Setup</b> dialog box. The following table describes the behavior for each possible value.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The remoted instance of Windows Media Player undocks, if necessary, and shows the device settings dialog box. If the Player is in skin mode, it returns to full mode. If the Player is locked in skin mode by corporate policy, the call fails.When the user closes the dialog box, Windows Media Player returns to its original docking state.

Note that the events for docking and undocking the Player will occur normally.

</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Windows Media Player attempts to create a partnership using a default set of device synchronization playlists. The Player does not change its current visible state or mode.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded or a partnership exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NO_PDA (0xC00D1179L)</b></dt>
</dl>
</td>
<td width="60%">
The device is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_MANUALDEVICE (0xC00D1183)</b></dt>
</dl>
</td>
<td width="60%">
The status for the current device is wmpdsManualDevice.

</td>
</tr>
</table>
 




## -remarks



This method starts the asynchronous process of creating a partnership. To get the result, you must handle the <b>CreatePartnershipComplete</b> event. If the partnership exists already, this method returns S_OK and no event occurs.

Windows Media Player 10 or later supports up to 16 device partnerships. The Player allows one partnership with one computer for each device. This means that creating a new partnership destroys any existing partnership with the current device.

Windows Media Player cannot create a partnership with a device having the status wmpdsManualDevice.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/3cd9b27d-ceb4-4655-ab3f-3d341774c81a">IWMPEvents2::CreatePartnershipComplete</a>



<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice Interface</a>



<a href="https://msdn.microsoft.com/36d40dc4-5641-49dd-9ef4-31d2acd0f41d">IWMPSyncDevice::get_deviceId</a>
 

 

