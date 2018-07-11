---
UID: NF:wmp.IWMPSyncDevice.get_friendlyName
title: IWMPSyncDevice::get_friendlyName
author: windows-sdk-content
description: The get_friendlyName method retrieves the user-defined name of the device.
old-location: wmp\iwmpsyncdevice_get_friendlyname.htm
old-project: WMP
ms.assetid: f72eaa17-fd7a-4844-8380-1a2547644dee
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_friendlyName method, IWMPSyncDevice.get_friendlyName, IWMPSyncDevice::get_friendlyName, IWMPSyncDeviceget_friendlyName, get_friendlyName, get_friendlyName method [Windows Media Player], get_friendlyName method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_friendlyname, wmp/IWMPSyncDevice::get_friendlyName
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSyncDevice.get_friendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSyncDevice::get_friendlyName


## -description



The <b>get_friendlyName</b> method retrieves the user-defined name of the device.




## -parameters




### -param pbstrName [out]

Pointer to a <b>BSTR</b> that contains the friendly name.


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



The friendly name is the device name that appears in the Windows Media Player user interface.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice Interface</a>



<a href="https://msdn.microsoft.com/caea8f34-8d0c-49ce-ae86-fda6c6b0b68b">IWMPSyncDevice::put_friendlyName</a>



<a href="https://msdn.microsoft.com/c553d495-d8fc-4483-a3dc-6679c6b9d1f1">Retrieving Device Attributes</a>
 

 

