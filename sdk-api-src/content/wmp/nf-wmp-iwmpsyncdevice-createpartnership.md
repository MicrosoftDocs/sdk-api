---
UID: NF:wmp.IWMPSyncDevice.createPartnership
title: IWMPSyncDevice::createPartnership (wmp.h)
description: The createPartnership method creates a partnership between Windows Media Player and the device.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","createPartnership method","IWMPSyncDevice.createPartnership","IWMPSyncDevice::createPartnership","IWMPSyncDevicecreatePartnership","createPartnership","createPartnership method [Windows Media Player]","createPartnership method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_createpartnership","wmp/IWMPSyncDevice::createPartnership"]
old-location: wmp\iwmpsyncdevice_createpartnership.htm
tech.root: WMP
ms.assetid: 734a8717-3b7f-4a40-895f-b55cfabd665c
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice interface [Windows Media Player],createPartnership method, IWMPSyncDevice.createPartnership, IWMPSyncDevice::createPartnership, IWMPSyncDevicecreatePartnership, createPartnership, createPartnership method [Windows Media Player], createPartnership method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_createpartnership, wmp/IWMPSyncDevice::createPartnership
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
 - IWMPSyncDevice::createPartnership
 - wmp/IWMPSyncDevice::createPartnership
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
 - IWMPSyncDevice.createPartnership
---

# IWMPSyncDevice::createPartnership


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>createPartnership</b> method creates a partnership between Windows Media Player and the device.

## -parameters

### -param vbShowUI [out]

<b>VARIANT_BOOL</b> that specifies whether Windows Media Player displays the <b>Device Setup</b> dialog box. The following table describes the behavior for each possible value.

<table>
<tr>
<th>Value
                </th>
<th>Description
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

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents2-createpartnershipcomplete">IWMPEvents2::CreatePartnershipComplete</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_deviceid">IWMPSyncDevice::get_deviceId</a>