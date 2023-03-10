---
UID: NF:wmp.IWMPSyncDevice.get_friendlyName
title: IWMPSyncDevice::get_friendlyName (wmp.h)
description: The get_friendlyName method retrieves the user-defined name of the device.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","get_friendlyName method","IWMPSyncDevice.get_friendlyName","IWMPSyncDevice::get_friendlyName","IWMPSyncDeviceget_friendlyName","get_friendlyName","get_friendlyName method [Windows Media Player]","get_friendlyName method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_get_friendlyname","wmp/IWMPSyncDevice::get_friendlyName"]
old-location: wmp\iwmpsyncdevice_get_friendlyname.htm
tech.root: WMP
ms.assetid: f72eaa17-fd7a-4844-8380-1a2547644dee
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_friendlyName method, IWMPSyncDevice.get_friendlyName, IWMPSyncDevice::get_friendlyName, IWMPSyncDeviceget_friendlyName, get_friendlyName, get_friendlyName method [Windows Media Player], get_friendlyName method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_friendlyname, wmp/IWMPSyncDevice::get_friendlyName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSyncDevice::get_friendlyName
 - wmp/IWMPSyncDevice::get_friendlyName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSyncDevice.get_friendlyName
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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-put_friendlyname">IWMPSyncDevice::put_friendlyName</a>



<a href="/windows/desktop/WMP/retrieving-device-attributes">Retrieving Device Attributes</a>