---
UID: NF:wmp.IWMPControls.previous
title: IWMPControls::previous (wmp.h)
description: The previous method sets the previous item in the playlist as the current item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","previous method","IWMPControls.previous","IWMPControls::previous","IWMPControlsprevious","previous","previous method [Windows Media Player]","previous method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_previous","wmp/IWMPControls::previous"]
old-location: wmp\iwmpcontrols_previous.htm
tech.root: WMP
ms.assetid: e26eca59-1e2d-4a1f-b133-e337a934014b
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],previous method, IWMPControls.previous, IWMPControls::previous, IWMPControlsprevious, previous, previous method [Windows Media Player], previous method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_previous, wmp/IWMPControls::previous
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
 - IWMPControls::previous
 - wmp/IWMPControls::previous
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
 - IWMPControls.previous
---

# IWMPControls::previous


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>previous</b> method sets the previous item in the playlist as the current item.



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

If the playlist is on the first entry when <b>previous</b> is invoked, the last entry in the playlist will become the current one.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-next">IWMPControls::next</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-stop">IWMPControls::stop</a>
