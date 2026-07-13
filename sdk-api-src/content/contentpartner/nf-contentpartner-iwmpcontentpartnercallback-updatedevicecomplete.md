---
UID: NF:contentpartner.IWMPContentPartnerCallback.UpdateDeviceComplete
title: IWMPContentPartnerCallback::UpdateDeviceComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","UpdateDeviceComplete method","IWMPContentPartnerCallback.UpdateDeviceComplete","IWMPContentPartnerCallback::UpdateDeviceComplete","IWMPContentPartnerCallbackUpdateDeviceComplete","UpdateDeviceComplete","UpdateDeviceComplete method [Windows Media Player]","UpdateDeviceComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::UpdateDeviceComplete","wmp.iwmpcontentpartnercallback_updatedevicecomplete"]
old-location: wmp\iwmpcontentpartnercallback_updatedevicecomplete.htm
tech.root: WMP
ms.assetid: 0d21d9a0-1a7c-4f4e-9c9d-36a0d30ea63f
ms.date: 4/26/2023
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],UpdateDeviceComplete method, IWMPContentPartnerCallback.UpdateDeviceComplete, IWMPContentPartnerCallback::UpdateDeviceComplete, IWMPContentPartnerCallbackUpdateDeviceComplete, UpdateDeviceComplete, UpdateDeviceComplete method [Windows Media Player], UpdateDeviceComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::UpdateDeviceComplete, wmp.iwmpcontentpartnercallback_updatedevicecomplete
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPContentPartnerCallback::UpdateDeviceComplete
 - contentpartner/IWMPContentPartnerCallback::UpdateDeviceComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartnerCallback.UpdateDeviceComplete
---

# IWMPContentPartnerCallback::UpdateDeviceComplete


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>UpdateDeviceComplete</b> method notifies Windows Media Player that the online store has finished processing a call to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice">IWMPContentPartner::UpdateDevice</a>.

## -parameters

### -param bstrDeviceName [in]

String containing the device name.

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
</table>

## -remarks

This method should be called in response to <b>UpdateDevice</b>, following the completion of the device update.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>