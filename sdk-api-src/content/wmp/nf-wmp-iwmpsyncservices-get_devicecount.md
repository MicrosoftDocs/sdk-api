---
UID: NF:wmp.IWMPSyncServices.get_deviceCount
title: IWMPSyncServices::get_deviceCount (wmp.h)
description: The get_deviceCount method retrieves the number of available devices.
helpviewer_keywords: ["IWMPSyncServices interface [Windows Media Player]","get_deviceCount method","IWMPSyncServices.get_deviceCount","IWMPSyncServices::get_deviceCount","IWMPSyncServicesget_deviceCount","get_deviceCount","get_deviceCount method [Windows Media Player]","get_deviceCount method [Windows Media Player]","IWMPSyncServices interface","wmp.iwmpsyncservices_get_devicecount","wmp/IWMPSyncServices::get_deviceCount"]
old-location: wmp\iwmpsyncservices_get_devicecount.htm
tech.root: WMP
ms.assetid: dde5b3c8-ea22-403c-ae69-05dc7f2efdda
ms.date: 4/26/2023
ms.keywords: IWMPSyncServices interface [Windows Media Player],get_deviceCount method, IWMPSyncServices.get_deviceCount, IWMPSyncServices::get_deviceCount, IWMPSyncServicesget_deviceCount, get_deviceCount, get_deviceCount method [Windows Media Player], get_deviceCount method [Windows Media Player],IWMPSyncServices interface, wmp.iwmpsyncservices_get_devicecount, wmp/IWMPSyncServices::get_deviceCount
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
 - IWMPSyncServices::get_deviceCount
 - wmp/IWMPSyncServices::get_deviceCount
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
 - IWMPSyncServices.get_deviceCount
---

# IWMPSyncServices::get_deviceCount


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_deviceCount</b> method retrieves the number of available devices.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> that contains the device count.

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

This method may return devices that have been connected previously, but that do not have a partnership established. Therefore, the list of returned devices does not represent a list of devices with partnerships.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices">IWMPSyncServices Interface</a>