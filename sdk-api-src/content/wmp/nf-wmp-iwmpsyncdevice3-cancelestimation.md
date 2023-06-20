---
UID: NF:wmp.IWMPSyncDevice3.cancelEstimation
title: IWMPSyncDevice3::cancelEstimation (wmp.h)
description: The cancelEstimation method cancels an estimation that was previously initiated by estimateSyncSize.
helpviewer_keywords: ["IWMPSyncDevice3 interface [Windows Media Player]","cancelEstimation method","IWMPSyncDevice3.cancelEstimation","IWMPSyncDevice3::cancelEstimation","cancelEstimation","cancelEstimation method [Windows Media Player]","cancelEstimation method [Windows Media Player]","IWMPSyncDevice3 interface","wmp.iwmpsyncdevice3_cancelestimation","wmp/IWMPSyncDevice3::cancelEstimation"]
old-location: wmp\iwmpsyncdevice3_cancelestimation.htm
tech.root: WMP
ms.assetid: 82e87e44-0a38-43c0-bbed-011581ae8a85
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice3 interface [Windows Media Player],cancelEstimation method, IWMPSyncDevice3.cancelEstimation, IWMPSyncDevice3::cancelEstimation, cancelEstimation, cancelEstimation method [Windows Media Player], cancelEstimation method [Windows Media Player],IWMPSyncDevice3 interface, wmp.iwmpsyncdevice3_cancelestimation, wmp/IWMPSyncDevice3::cancelEstimation
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 12
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
 - IWMPSyncDevice3::cancelEstimation
 - wmp/IWMPSyncDevice3::cancelEstimation
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
 - IWMPSyncDevice3.cancelEstimation
---

# IWMPSyncDevice3::cancelEstimation


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>cancelEstimation</b> method cancels an estimation that was previously initiated by <a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize">estimateSyncSize</a>.



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

When you call this method, Windows Media Player raises the<a href="/windows/desktop/WMP/iwmpevents4-syncestimationcomplete"> IWMPEvents4::SyncEstimationComplete</a> event with an <b>HRESULT</b> of E_ABORT.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3">IWMPSyncDevice3 Interface</a>
