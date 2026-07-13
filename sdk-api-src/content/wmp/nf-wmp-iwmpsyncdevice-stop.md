---
UID: NF:wmp.IWMPSyncDevice.stop
title: IWMPSyncDevice::stop (wmp.h)
description: The stop method ends synchronization.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","stop method","IWMPSyncDevice.stop","IWMPSyncDevice::stop","IWMPSyncDevicestop","stop","stop method [Windows Media Player]","stop method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_stop","wmp/IWMPSyncDevice::stop"]
old-location: wmp\iwmpsyncdevice_stop.htm
tech.root: WMP
ms.assetid: 30e6787e-851b-420c-934c-5f8e5e4d83df
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice interface [Windows Media Player],stop method, IWMPSyncDevice.stop, IWMPSyncDevice::stop, IWMPSyncDevicestop, stop, stop method [Windows Media Player], stop method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_stop, wmp/IWMPSyncDevice::stop
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
 - IWMPSyncDevice::stop
 - wmp/IWMPSyncDevice::stop
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
 - IWMPSyncDevice.stop
---

# IWMPSyncDevice::stop


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>stop</b> method ends synchronization.



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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start">IWMPSyncDevice::start</a>
