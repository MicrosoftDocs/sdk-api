---
UID: NF:wmp.IWMPNetwork.get_bufferingProgress
title: IWMPNetwork::get_bufferingProgress (wmp.h)
description: The get_bufferingProgress method retrieves the percentage of buffering completed.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_bufferingProgress method","IWMPNetwork.get_bufferingProgress","IWMPNetwork::get_bufferingProgress","IWMPNetworkget_bufferingProgress","get_bufferingProgress","get_bufferingProgress method [Windows Media Player]","get_bufferingProgress method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_bufferingprogress","wmp/IWMPNetwork::get_bufferingProgress"]
old-location: wmp\iwmpnetwork_get_bufferingprogress.htm
tech.root: WMP
ms.assetid: 5c8cc541-3fc2-49b8-8a1a-f4959989aafe
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bufferingProgress method, IWMPNetwork.get_bufferingProgress, IWMPNetwork::get_bufferingProgress, IWMPNetworkget_bufferingProgress, get_bufferingProgress, get_bufferingProgress method [Windows Media Player], get_bufferingProgress method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bufferingprogress, wmp/IWMPNetwork::get_bufferingProgress
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
 - IWMPNetwork::get_bufferingProgress
 - wmp/IWMPNetwork::get_bufferingProgress
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
 - IWMPNetwork.get_bufferingProgress
---

# IWMPNetwork::get_bufferingProgress


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_bufferingProgress</b> method retrieves the percentage of buffering completed.

## -parameters

### -param plBufferingProgress [out]

Pointer to a <b>long</b> containing the buffering progress.

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

Each time playback is stopped and restarted, the value retrieved from this method is zero. It is not reset if playback is paused.

Buffering only applies to streaming content. This method retrieves valid information only during run time when the URL for playback is set using the <b>IWMPCore::put_URL</b> method.

Use the <b>IWMPEvents::Buffering</b> event to determine when buffering starts or stops.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-buffering">IWMPEvents::Buffering</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>