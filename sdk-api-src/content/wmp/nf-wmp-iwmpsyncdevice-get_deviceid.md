---
UID: NF:wmp.IWMPSyncDevice.get_deviceId
title: IWMPSyncDevice::get_deviceId (wmp.h)
description: The get_deviceId method retrieves the device identifier string.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","get_deviceId method","IWMPSyncDevice.get_deviceId","IWMPSyncDevice::get_deviceId","IWMPSyncDeviceget_deviceId","get_deviceId","get_deviceId method [Windows Media Player]","get_deviceId method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_get_deviceid","wmp/IWMPSyncDevice::get_deviceId"]
old-location: wmp\iwmpsyncdevice_get_deviceid.htm
tech.root: WMP
ms.assetid: 36d40dc4-5641-49dd-9ef4-31d2acd0f41d
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_deviceId method, IWMPSyncDevice.get_deviceId, IWMPSyncDevice::get_deviceId, IWMPSyncDeviceget_deviceId, get_deviceId, get_deviceId method [Windows Media Player], get_deviceId method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_deviceid, wmp/IWMPSyncDevice::get_deviceId
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
 - IWMPSyncDevice::get_deviceId
 - wmp/IWMPSyncDevice::get_deviceId
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
 - IWMPSyncDevice.get_deviceId
---

# IWMPSyncDevice::get_deviceId


## -description

The <b>get_deviceId</b> method retrieves the device identifier string.

## -parameters

### -param pbstrDeviceId [out]

Address of a <b>BSTR</b> variable that receives a string containing the device identifier.

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

The device identifier is the serial number for the device. This value is not guaranteed to be unique for mass storage devices. However, it is unlikely that a particular user will encounter duplicate serial numbers.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex">IWMPSyncDevice::get_partnershipIndex</a>



<a href="/windows/desktop/WMP/retrieving-device-attributes">Retrieving Device Attributes</a>