---
UID: NF:wmp.IWMPSyncDevice.showSettings
title: IWMPSyncDevice::showSettings (wmp.h)
description: The showSettings method displays the Windows Media Player synchronization settings dialog box.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","showSettings method","IWMPSyncDevice.showSettings","IWMPSyncDevice::showSettings","IWMPSyncDeviceshowSettings","showSettings","showSettings method [Windows Media Player]","showSettings method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_showsettings","wmp/IWMPSyncDevice::showSettings"]
old-location: wmp\iwmpsyncdevice_showsettings.htm
tech.root: WMP
ms.assetid: 496bb3b6-d942-4d53-8e66-5aed5f574343
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice interface [Windows Media Player],showSettings method, IWMPSyncDevice.showSettings, IWMPSyncDevice::showSettings, IWMPSyncDeviceshowSettings, showSettings, showSettings method [Windows Media Player], showSettings method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_showsettings, wmp/IWMPSyncDevice::showSettings
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
 - IWMPSyncDevice::showSettings
 - wmp/IWMPSyncDevice::showSettings
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
 - IWMPSyncDevice.showSettings
---

# IWMPSyncDevice::showSettings


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>showSettings</b> method displays the Windows Media Player synchronization settings dialog box.



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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_PARTNERSHIPNOTEXIST</b></dt>
</dl>
</td>
<td width="60%">
The current status for the device is wmpdsPartnershipDeclined, wmpdsPartnershipAnother, or wmpdsNewDevice. This method only shows the settings dialog box for devices for which a partnership exists with the current instance of Windows Media Player.

</td>
</tr>
</table>

## -remarks

The remoted instance of Windows Media Player undocks, if necessary, and shows the device settings dialog box. If the Player was in skin mode, it returns to full mode. If the Player is locked in skin mode by corporate policy, the call fails.

When the user closes the dialog box, Windows Media Player returns to its original docking state.

Note that the events for docking and undocking Windows Media Player will occur normally.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>
