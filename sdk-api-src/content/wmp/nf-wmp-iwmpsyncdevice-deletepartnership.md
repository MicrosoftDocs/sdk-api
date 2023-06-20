---
UID: NF:wmp.IWMPSyncDevice.deletePartnership
title: IWMPSyncDevice::deletePartnership (wmp.h)
description: The deletePartnership method terminates the partnership between Windows Media Player and the device.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","deletePartnership method","IWMPSyncDevice.deletePartnership","IWMPSyncDevice::deletePartnership","IWMPSyncDevicedeletePartnership","deletePartnership","deletePartnership method [Windows Media Player]","deletePartnership method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_deletepartnership","wmp/IWMPSyncDevice::deletePartnership"]
old-location: wmp\iwmpsyncdevice_deletepartnership.htm
tech.root: WMP
ms.assetid: ecb525b4-c804-47e6-8d6c-7d943010077a
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice interface [Windows Media Player],deletePartnership method, IWMPSyncDevice.deletePartnership, IWMPSyncDevice::deletePartnership, IWMPSyncDevicedeletePartnership, deletePartnership, deletePartnership method [Windows Media Player], deletePartnership method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_deletepartnership, wmp/IWMPSyncDevice::deletePartnership
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
 - IWMPSyncDevice::deletePartnership
 - wmp/IWMPSyncDevice::deletePartnership
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
 - IWMPSyncDevice.deletePartnership
---

# IWMPSyncDevice::deletePartnership


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>deletePartnership</b> method terminates the partnership between Windows Media Player and the device.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but there was no partnership to delete. This occurs when the current status is wmpdsPartnershipDeclined or wmpdsNewDevice.

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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_PARTNERSHIPNOTEXIST (0xC00D1184)</b></dt>
</dl>
</td>
<td width="60%">
The method failed because the current status for the device is wmpdsPartnershipAnother. This method will only delete partnerships that exist for the current instance of Windows Media Player.

</td>
</tr>
</table>

## -remarks

When the partnership is deleted, the device status is set to <b>wmpdsPartnershipDeclined</b>. If no partnership exists, this method simply returns S_OK.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>
