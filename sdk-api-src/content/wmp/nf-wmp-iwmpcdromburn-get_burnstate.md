---
UID: NF:wmp.IWMPCdromBurn.get_burnState
title: IWMPCdromBurn::get_burnState (wmp.h)
description: The get_burnState method retrieves an enumeration value that indicates the current burn state.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","get_burnState method","IWMPCdromBurn.get_burnState","IWMPCdromBurn::get_burnState","IWMPCdromBurnget_burnState","get_burnState","get_burnState method [Windows Media Player]","get_burnState method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_get_burnstate","wmp/IWMPCdromBurn::get_burnState"]
old-location: wmp\iwmpcdromburn_get_burnstate.htm
tech.root: WMP
ms.assetid: a6bcb8d6-07ad-4d8f-a94a-6b8c1b7f0c2b
ms.date: 4/26/2023
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnState method, IWMPCdromBurn.get_burnState, IWMPCdromBurn::get_burnState, IWMPCdromBurnget_burnState, get_burnState, get_burnState method [Windows Media Player], get_burnState method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnstate, wmp/IWMPCdromBurn::get_burnState
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
 - IWMPCdromBurn::get_burnState
 - wmp/IWMPCdromBurn::get_burnState
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
 - IWMPCdromBurn.get_burnState
---

# IWMPCdromBurn::get_burnState


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_burnState</b> method retrieves an enumeration value that indicates the current burn state.

## -parameters

### -param pwmpbs [out]

Pointer to a variable that receives a value from the <b>WMPBurnState</b> enumeration that indicates the current state.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpburnstate">WMPBurnState</a>