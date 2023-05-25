---
UID: NF:wmp.IWMPSyncServices.getDevice
title: IWMPSyncServices::getDevice (wmp.h)
description: The getDevice method retrieves a pointer to a device interface.
helpviewer_keywords: ["IWMPSyncServices interface [Windows Media Player]","getDevice method","IWMPSyncServices.getDevice","IWMPSyncServices::getDevice","IWMPSyncServicesgetDevice","getDevice","getDevice method [Windows Media Player]","getDevice method [Windows Media Player]","IWMPSyncServices interface","wmp.iwmpsyncservices_getdevice","wmp/IWMPSyncServices::getDevice"]
old-location: wmp\iwmpsyncservices_getdevice.htm
tech.root: WMP
ms.assetid: 4c34b823-57ce-4053-9e98-308a5d4ffdef
ms.date: 4/26/2023
ms.keywords: IWMPSyncServices interface [Windows Media Player],getDevice method, IWMPSyncServices.getDevice, IWMPSyncServices::getDevice, IWMPSyncServicesgetDevice, getDevice, getDevice method [Windows Media Player], getDevice method [Windows Media Player],IWMPSyncServices interface, wmp.iwmpsyncservices_getdevice, wmp/IWMPSyncServices::getDevice
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
 - IWMPSyncServices::getDevice
 - wmp/IWMPSyncServices::getDevice
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
 - IWMPSyncServices.getDevice
---

# IWMPSyncServices::getDevice


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getDevice</b> method retrieves a pointer to a device interface.

## -parameters

### -param lIndex [in]

<b>long</b> that contains the index of the device to retrieve. Device indexes are zero-based.

### -param ppDevice [out]

Pointer to a pointer to an <b>IWMPSyncDevice</b> interface that represents the device having the specified index.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices">IWMPSyncServices Interface</a>