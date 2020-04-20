---
UID: NF:wmp.IWMPSyncDevice.put_friendlyName
title: IWMPSyncDevice::put_friendlyName (wmp.h)
description: The put_friendlyName method specifies the user-defined name of the device.helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","put_friendlyName method","IWMPSyncDevice.put_friendlyName","IWMPSyncDevice::put_friendlyName","IWMPSyncDeviceput_friendlyName","put_friendlyName","put_friendlyName method [Windows Media Player]","put_friendlyName method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_put_friendlyname","wmp/IWMPSyncDevice::put_friendlyName"]
old-location: wmp\iwmpsyncdevice_put_friendlyname.htm
tech.root: WMP
ms.assetid: caea8f34-8d0c-49ce-ae86-fda6c6b0b68b
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],put_friendlyName method, IWMPSyncDevice.put_friendlyName, IWMPSyncDevice::put_friendlyName, IWMPSyncDeviceput_friendlyName, put_friendlyName, put_friendlyName method [Windows Media Player], put_friendlyName method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_put_friendlyname, wmp/IWMPSyncDevice::put_friendlyName
f1_keywords:
- wmp/IWMPSyncDevice.put_friendlyName
dev_langs:
- c++
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPSyncDevice.put_friendlyName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice::put_friendlyName


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_friendlyname">IWMPSyncDevice::get_friendlyName</a>
 

 

