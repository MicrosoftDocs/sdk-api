---
UID: NF:wmp.IWMPSyncDevice.showSettings
title: IWMPSyncDevice::showSettings (wmp.h)
description: The showSettings method displays the Windows Media Player synchronization settings dialog box.helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","showSettings method","IWMPSyncDevice.showSettings","IWMPSyncDevice::showSettings","IWMPSyncDeviceshowSettings","showSettings","showSettings method [Windows Media Player]","showSettings method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_showsettings","wmp/IWMPSyncDevice::showSettings"]
old-location: wmp\iwmpsyncdevice_showsettings.htm
tech.root: WMP
ms.assetid: 496bb3b6-d942-4d53-8e66-5aed5f574343
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],showSettings method, IWMPSyncDevice.showSettings, IWMPSyncDevice::showSettings, IWMPSyncDeviceshowSettings, showSettings, showSettings method [Windows Media Player], showSettings method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_showsettings, wmp/IWMPSyncDevice::showSettings
f1_keywords:
- wmp/IWMPSyncDevice.showSettings
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
- IWMPSyncDevice.showSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice::showSettings


## -description



The <b>showSettings</b> method displays the Windows Media Player synchronization settings dialog box.




## -parameters






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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>
 

 

