---
UID: NF:wmp.IWMPPlayer.get_enableContextMenu
title: IWMPPlayer::get_enableContextMenu (wmp.h)
description: The get_enableContextMenu method retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.helpviewer_keywords: ["IWMPPlayer interface [Windows Media Player]","get_enableContextMenu method","IWMPPlayer.get_enableContextMenu","IWMPPlayer::get_enableContextMenu","IWMPPlayerget_enableContextMenu","get_enableContextMenu","get_enableContextMenu method [Windows Media Player]","get_enableContextMenu method [Windows Media Player]","IWMPPlayer interface","wmp.iwmpplayer_get_enablecontextmenu","wmp/IWMPPlayer::get_enableContextMenu"]
old-location: wmp\iwmpplayer_get_enablecontextmenu.htm
tech.root: WMP
ms.assetid: 66769441-7923-45d2-b84f-24770537923c
ms.date: 12/05/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],get_enableContextMenu method, IWMPPlayer.get_enableContextMenu, IWMPPlayer::get_enableContextMenu, IWMPPlayerget_enableContextMenu, get_enableContextMenu, get_enableContextMenu method [Windows Media Player], get_enableContextMenu method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_get_enablecontextmenu, wmp/IWMPPlayer::get_enableContextMenu
f1_keywords:
- wmp/IWMPPlayer.get_enableContextMenu
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPPlayer.get_enableContextMenu
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer::get_enableContextMenu


## -description



The <b>get_enableContextMenu</b> method retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.




## -parameters




### -param pbEnableContextMenu [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether to the enable context menu. The default is <b>TRUE</b>.


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



During full-screen playback, Windows Media Player hides the mouse cursor when the <b>VARIANT_BOOL</b> retrieved by <b>get_enableContextMenu</b> equals <b>FALSE</b> and the <b>BSTR</b> retrieved by <b>IWMPPlayer::get_uiMode</b> equals "none".

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enabled">IWMPPlayer::get_enabled</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_uimode">IWMPPlayer::get_uiMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_enablecontextmenu">IWMPPlayer::put_enableContextMenu</a>
 

 

