---
UID: NF:wmp.IWMPCdromRip.get_ripProgress
title: IWMPCdromRip::get_ripProgress (wmp.h)
description: The get_ripProgress method retrieves the CD ripping progress as percent complete.
helpviewer_keywords: ["IWMPCdromRip interface [Windows Media Player]","get_ripProgress method","IWMPCdromRip.get_ripProgress","IWMPCdromRip::get_ripProgress","IWMPCdromRipget_ripProgress","get_ripProgress","get_ripProgress method [Windows Media Player]","get_ripProgress method [Windows Media Player]","IWMPCdromRip interface","wmp.iwmpcdromrip_get_ripprogress","wmp/IWMPCdromRip::get_ripProgress"]
old-location: wmp\iwmpcdromrip_get_ripprogress.htm
tech.root: WMP
ms.assetid: d7140bc9-bf79-48f0-aaf0-155660c8b2c9
ms.date: 4/26/2023
ms.keywords: IWMPCdromRip interface [Windows Media Player],get_ripProgress method, IWMPCdromRip.get_ripProgress, IWMPCdromRip::get_ripProgress, IWMPCdromRipget_ripProgress, get_ripProgress, get_ripProgress method [Windows Media Player], get_ripProgress method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_get_ripprogress, wmp/IWMPCdromRip::get_ripProgress
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromRip::get_ripProgress
 - wmp/IWMPCdromRip::get_ripProgress
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
 - IWMPCdromRip.get_ripProgress
---

# IWMPCdromRip::get_ripProgress


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_ripProgress</b> method retrieves the CD ripping progress as percent complete.

## -parameters

### -param plProgress [out]

Pointer to a <b>long</b> that receives the progress value. Progress values range from 0 to 100.

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

The progress value represents the completed percentage of the entire ripping process. To determine the progress of a specific track, use <a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">IWMPMedia::getItemInfo</a> with <b>RipProgress</b> as the attribute name. To determine the index of the track currently being ripped, call <a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-getiteminfo">IWMPPlaylist::getItemInfo</a> with <b>CurrentRipTrackIndex</b> as the attribute name.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>



<a href="/windows/desktop/WMP/ripping-a-cd">Ripping a CD</a>