---
UID: NF:wmp.IWMPControls2.step
title: IWMPControls2::step (wmp.h)
description: The step method causes the current video media item to freeze playback on the next frame or the previous frame.
helpviewer_keywords: ["IWMPControls2 interface [Windows Media Player]","step method","IWMPControls2.step","IWMPControls2::step","IWMPControls2step","step","step method [Windows Media Player]","step method [Windows Media Player]","IWMPControls2 interface","wmp.iwmpcontrols2_step","wmp/IWMPControls2::step"]
old-location: wmp\iwmpcontrols2_step.htm
tech.root: WMP
ms.assetid: d54a4bb7-855f-4807-89b5-176b7fac2edd
ms.date: 4/26/2023
ms.keywords: IWMPControls2 interface [Windows Media Player],step method, IWMPControls2.step, IWMPControls2::step, IWMPControls2step, step, step method [Windows Media Player], step method [Windows Media Player],IWMPControls2 interface, wmp.iwmpcontrols2_step, wmp/IWMPControls2::step
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
 - IWMPControls2::step
 - wmp/IWMPControls2::step
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
 - IWMPControls2.step
---

# IWMPControls2::step


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>step</b> method causes the current video media item to freeze playback on the next frame or the previous frame.

## -parameters

### -param lStep [in]

<b>long</b> indicating how many frames to step before freezing. Must be set to 1 or -1.

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

This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2">IWMPControls2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>