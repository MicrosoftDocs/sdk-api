---
UID: NF:wmp.IWMPSyncDevice.start
title: IWMPSyncDevice::start (wmp.h)
description: The start method begins synchronization.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","start method","IWMPSyncDevice.start","IWMPSyncDevice::start","IWMPSyncDevicestart","start","start method [Windows Media Player]","start method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_start","wmp/IWMPSyncDevice::start"]
old-location: wmp\iwmpsyncdevice_start.htm
tech.root: WMP
ms.assetid: f12e5abe-3d1b-48ab-8a03-420a40ae8b4f
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],start method, IWMPSyncDevice.start, IWMPSyncDevice::start, IWMPSyncDevicestart, start, start method [Windows Media Player], start method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_start, wmp/IWMPSyncDevice::start
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
 - IWMPSyncDevice::start
 - wmp/IWMPSyncDevice::start
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
 - IWMPSyncDevice.start
---

# IWMPSyncDevice::start


## -description

The <b>start</b> method begins synchronization.

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
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
</table>

## -remarks

Synchronization rules for a particular device are defined by the user in Windows Media Player. This method only starts the synchronization process.

Synchronization should not be confused with transferring, which is a manual operation in Windows Media Player. The Windows Media Player SDK does not provide methods for transferring digital media to a device.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop">IWMPSyncDevice::stop</a>