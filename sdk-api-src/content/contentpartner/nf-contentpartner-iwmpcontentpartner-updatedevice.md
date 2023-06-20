---
UID: NF:contentpartner.IWMPContentPartner.UpdateDevice
title: IWMPContentPartner::UpdateDevice (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","UpdateDevice method","IWMPContentPartner.UpdateDevice","IWMPContentPartner::UpdateDevice","IWMPContentPartnerUpdateDevice","UpdateDevice","UpdateDevice method [Windows Media Player]","UpdateDevice method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::UpdateDevice","wmp.iwmpcontentpartner_updatedevice"]
old-location: wmp\iwmpcontentpartner_updatedevice.htm
tech.root: WMP
ms.assetid: 893beb65-048f-4496-88e6-b0e0b8db0205
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner interface [Windows Media Player],UpdateDevice method, IWMPContentPartner.UpdateDevice, IWMPContentPartner::UpdateDevice, IWMPContentPartnerUpdateDevice, UpdateDevice, UpdateDevice method [Windows Media Player], UpdateDevice method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::UpdateDevice, wmp.iwmpcontentpartner_updatedevice
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
 - IWMPContentPartner::UpdateDevice
 - contentpartner/IWMPContentPartner::UpdateDevice
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
 - IWMPContentPartner.UpdateDevice
---

# IWMPContentPartner::UpdateDevice


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>UpdateDevice</b> method notifies the content partner plug-in that a portable device is being synchronized.

## -parameters

### -param bstrDeviceName [in]

<b>BSTR</b> containing the device name.

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

You must call <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete">IWMPContentPartnerCallback::UpdateDeviceComplete</a> exactly once for each call to <b>UpdateDevice</b> from which you return a success code.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>