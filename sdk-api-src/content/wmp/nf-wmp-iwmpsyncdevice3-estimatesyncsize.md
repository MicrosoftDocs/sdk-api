---
UID: NF:wmp.IWMPSyncDevice3.estimateSyncSize
title: IWMPSyncDevice3::estimateSyncSize (wmp.h)
description: The estimateSyncSize method initiates the estimation of the size required on the device to synchronize a specified playlist.
helpviewer_keywords: ["IWMPSyncDevice3 interface [Windows Media Player]","estimateSyncSize method","IWMPSyncDevice3.estimateSyncSize","IWMPSyncDevice3::estimateSyncSize","estimateSyncSize","estimateSyncSize method [Windows Media Player]","estimateSyncSize method [Windows Media Player]","IWMPSyncDevice3 interface","wmp.iwmpsyncdevice3_estimatesyncsize","wmp/IWMPSyncDevice3::estimateSyncSize"]
old-location: wmp\iwmpsyncdevice3_estimatesyncsize.htm
tech.root: WMP
ms.assetid: 49b07233-df9d-4fd0-836e-62b992408018
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice3 interface [Windows Media Player],estimateSyncSize method, IWMPSyncDevice3.estimateSyncSize, IWMPSyncDevice3::estimateSyncSize, estimateSyncSize, estimateSyncSize method [Windows Media Player], estimateSyncSize method [Windows Media Player],IWMPSyncDevice3 interface, wmp.iwmpsyncdevice3_estimatesyncsize, wmp/IWMPSyncDevice3::estimateSyncSize
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
 - IWMPSyncDevice3::estimateSyncSize
 - wmp/IWMPSyncDevice3::estimateSyncSize
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
 - IWMPSyncDevice3.estimateSyncSize
---

# IWMPSyncDevice3::estimateSyncSize


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>estimateSyncSize</b> method initiates the estimation of the size required on the device to synchronize a specified playlist.

## -parameters

### -param pNonRulePlaylist [in]

A pointer to an <a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist</a> interface that represents the playlist for which the size will be estimated. This parameter can be set to <b>NULL</b>. If this argument is specified the estimation will return the size of <i>pNonRulePlaylist</i> and the current sync rules, if any.

### -param pRulesPlaylist [in]

A pointer to an <a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist</a> interface that represents the playlist for which the size will be estimated. This parameter can be set to <b>NULL</b>. If this argument is specified then the current sync rules will be excluded from the estimation so that the estimation will return the size of <i>pNonRulePlaylist</i> and <i>pRulesPlaylist</i>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is shutting down, or <i>pNonRulePlaylist</i> and <i>pRulesPlaylist</i>  are both <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
A synchronization session is already in progress for the device.

</td>
</tr>
</table>

## -remarks

The estimation of required size is done asynchronously. That is, this method initiates the estimation and then returns immediately. When the estimation is complete, Windows Media Player raises the <a href="/windows/desktop/WMP/iwmpevents4-syncestimationcomplete">IWMPEvents4::SyncEstimationComplete</a> event.

The estimation cannot occur if a synchronization session is currently in progress for the device.

If you call this method and then call it again before the first estimation is complete, the first estimation is canceled and a new estimation is initiated.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3">IWMPSyncDevice3 Interface</a>