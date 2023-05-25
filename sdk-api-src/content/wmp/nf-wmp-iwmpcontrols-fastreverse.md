---
UID: NF:wmp.IWMPControls.fastReverse
title: IWMPControls::fastReverse (wmp.h)
description: The fastReverse method starts fast play of the media item in the reverse direction.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","fastReverse method","IWMPControls.fastReverse","IWMPControls::fastReverse","IWMPControlsfastReverse","fastReverse","fastReverse method [Windows Media Player]","fastReverse method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_fastreverse","wmp/IWMPControls::fastReverse"]
old-location: wmp\iwmpcontrols_fastreverse.htm
tech.root: WMP
ms.assetid: 2adec4c7-7aca-4191-8c6f-61e137188ad9
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],fastReverse method, IWMPControls.fastReverse, IWMPControls::fastReverse, IWMPControlsfastReverse, fastReverse, fastReverse method [Windows Media Player], fastReverse method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_fastreverse, wmp/IWMPControls::fastReverse
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
 - IWMPControls::fastReverse
 - wmp/IWMPControls::fastReverse
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
 - IWMPControls.fastReverse
---

# IWMPControls::fastReverse


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>fastReverse</b> method starts fast play of the media item in the reverse direction.



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

The <b>fastReverse</b> method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file. Calling <b>fastReverse</b> is equivalent to specifying -5.0 for the rate through the <b>IWMPSettings::put_rate</b> method. If the rate is subsequently changed, or if <b>IWMPControls::play</b> or <b>IWMPControls::stop</b> is called, Windows Media Player will cease fast reverse.

If the item is part of a playlist, <b>fastReverse</b> stops at the beginning of the current track. For instance, if track 3 is in <b>fastReverse</b>, when the beginning of track 3 is reached, Windows Media Player will not go to track 2. The play count is not incremented when calling <b>fastReverse</b>.

If you call <b>IWMPControls::fastForward</b> while <b>fastReverse</b> is running, <b>fastReverse</b> will be stopped and <b>IWMPControls::fastForward</b> will begin.

This method does not work for live broadcasts and certain digital media types. To determine whether you can use fast reverse in a clip, call the <b>IWMPControls::get_isAvailable</b> method and pass in the <b>BSTR</b> value "FastReverse".

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-fastforward">IWMPControls::fastForward</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_isavailable">IWMPControls::get_isAvailable</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-stop">IWMPControls::stop</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_rate">IWMPSettings::put_rate</a>
