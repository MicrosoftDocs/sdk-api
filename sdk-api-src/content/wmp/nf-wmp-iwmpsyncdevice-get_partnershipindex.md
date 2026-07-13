---
UID: NF:wmp.IWMPSyncDevice.get_partnershipIndex
title: IWMPSyncDevice::get_partnershipIndex (wmp.h)
description: The get_partnershipIndex method retrieves the index of the device partnership.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","get_partnershipIndex method","IWMPSyncDevice.get_partnershipIndex","IWMPSyncDevice::get_partnershipIndex","IWMPSyncDeviceget_partnershipIndex","get_partnershipIndex","get_partnershipIndex method [Windows Media Player]","get_partnershipIndex method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_get_partnershipindex","wmp/IWMPSyncDevice::get_partnershipIndex"]
old-location: wmp\iwmpsyncdevice_get_partnershipindex.htm
tech.root: WMP
ms.assetid: a7f04b97-8a09-4feb-b776-649aa9d6f407
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_partnershipIndex method, IWMPSyncDevice.get_partnershipIndex, IWMPSyncDevice::get_partnershipIndex, IWMPSyncDeviceget_partnershipIndex, get_partnershipIndex, get_partnershipIndex method [Windows Media Player], get_partnershipIndex method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_partnershipindex, wmp/IWMPSyncDevice::get_partnershipIndex
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
 - IWMPSyncDevice::get_partnershipIndex
 - wmp/IWMPSyncDevice::get_partnershipIndex
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
 - IWMPSyncDevice.get_partnershipIndex
---

# IWMPSyncDevice::get_partnershipIndex


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_partnershipIndex</b> method retrieves the index of the device partnership.

## -parameters

### -param plIndex [out]

Pointer to a <b>long</b> that contains the partnership index value. Possible values range from 0 to 16.

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

Windows Media Player 10 or later supports up to 16 device partnerships, numbered 1 to 16. The Player allows one partnership with one computer for each device. Creating a new partnership destroys any existing partnership with the current device.

When <i>plIndex</i> equals zero, no partnership exists.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership">IWMPSyncDevice::createPartnership</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership">IWMPSyncDevice::deletePartnership</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_deviceid">IWMPSyncDevice::get_deviceId</a>