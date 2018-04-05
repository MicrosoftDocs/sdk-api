---
UID: NF:wmp.IWMPSyncDevice.put_friendlyName
title: IWMPSyncDevice::put_friendlyName method
author: windows-driver-content
description: The put_friendlyName method specifies the user-defined name of the device.
old-location: wmp\iwmpsyncdevice_put_friendlyname.htm
old-project: WMP
ms.assetid: caea8f34-8d0c-49ce-ae86-fda6c6b0b68b
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPSyncDevice, IWMPSyncDevice interface [Windows Media Player], put_friendlyName method, IWMPSyncDevice::put_friendlyName, IWMPSyncDeviceput_friendlyName, put_friendlyName method [Windows Media Player], put_friendlyName method [Windows Media Player], IWMPSyncDevice interface, put_friendlyName,IWMPSyncDevice.put_friendlyName, wmp.iwmpsyncdevice_put_friendlyname, wmp/IWMPSyncDevice::put_friendlyName
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSyncDevice.put_friendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSyncDevice::put_friendlyName method


## -description



The <b>put_friendlyName</b> method specifies the user-defined name of the device.




## -parameters




### -param bstrName [in]

String containing the friendly name.


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
The method succeeded.

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
</table>
 




## -remarks



The friendly name is the string that is displayed in the Windows Media Player user interface to identify the device. For devices that support storing the friendly name on the device, this method also changes the friendly name on the device.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice Interface</a>



<a href="https://msdn.microsoft.com/f72eaa17-fd7a-4844-8380-1a2547644dee">IWMPSyncDevice::get_friendlyName</a>
 

 

