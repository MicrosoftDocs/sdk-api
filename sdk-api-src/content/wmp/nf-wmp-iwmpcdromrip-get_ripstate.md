---
UID: NF:wmp.IWMPCdromRip.get_ripState
title: IWMPCdromRip::get_ripState (wmp.h)
description: The get_ripState method retrieves an enumeration value that indicates the current state of the ripping process.
helpviewer_keywords: ["IWMPCdromRip interface [Windows Media Player]","get_ripState method","IWMPCdromRip.get_ripState","IWMPCdromRip::get_ripState","IWMPCdromRipget_ripState","get_ripState","get_ripState method [Windows Media Player]","get_ripState method [Windows Media Player]","IWMPCdromRip interface","wmp.iwmpcdromrip_get_ripstate","wmp/IWMPCdromRip::get_ripState"]
old-location: wmp\iwmpcdromrip_get_ripstate.htm
tech.root: WMP
ms.assetid: 81c7ba1d-81d7-4f64-9f7d-c88d6959bee0
ms.date: 4/26/2023
ms.keywords: IWMPCdromRip interface [Windows Media Player],get_ripState method, IWMPCdromRip.get_ripState, IWMPCdromRip::get_ripState, IWMPCdromRipget_ripState, get_ripState, get_ripState method [Windows Media Player], get_ripState method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_get_ripstate, wmp/IWMPCdromRip::get_ripState
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
 - IWMPCdromRip::get_ripState
 - wmp/IWMPCdromRip::get_ripState
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
 - IWMPCdromRip.get_ripState
---

# IWMPCdromRip::get_ripState


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_ripState</b> method retrieves an enumeration value that indicates the current state of the ripping process.

## -parameters

### -param pwmprs [out]

Pointer to a variable that receives a value from the <b>WMPRipState</b> enumeration that indicates the current state.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>



<a href="/windows/desktop/WMP/ripping-a-cd">Ripping a CD</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpripstate">WMPRipState</a>