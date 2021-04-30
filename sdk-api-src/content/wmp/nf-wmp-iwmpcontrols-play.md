---
UID: NF:wmp.IWMPControls.play
title: IWMPControls::play (wmp.h)
description: The play method causes the current media item to start playing, or resumes play of a paused item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","play method","IWMPControls.play","IWMPControls::play","IWMPControlsplay","play","play method [Windows Media Player]","play method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_play","wmp/IWMPControls::play"]
old-location: wmp\iwmpcontrols_play.htm
tech.root: WMP
ms.assetid: 45b5634b-6d23-4e61-90e4-ef0cc9d90a14
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],play method, IWMPControls.play, IWMPControls::play, IWMPControlsplay, play, play method [Windows Media Player], play method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_play, wmp/IWMPControls::play
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
 - IWMPControls::play
 - wmp/IWMPControls::play
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
 - IWMPControls.play
---

# IWMPControls::play


## -description

The <b>play</b> method causes the current media item to start playing, or resumes play of a paused item.

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
</table>

## -remarks

If this method is called while fast-forwarding or rewinding, the rate of playback is set to 1.0.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-playitem">IWMPControls::playItem</a>