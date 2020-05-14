---
UID: NF:wmp.IWMPPlayer.get_enabled
title: IWMPPlayer::get_enabled (wmp.h)
description: The get_enabled method retrieves a value indicating whether the Windows Media Player control is enabled.helpviewer_keywords: ["IWMPPlayer interface [Windows Media Player]","get_enabled method","IWMPPlayer.get_enabled","IWMPPlayer::get_enabled","IWMPPlayerget_enabled","get_enabled","get_enabled method [Windows Media Player]","get_enabled method [Windows Media Player]","IWMPPlayer interface","wmp.iwmpplayer_get_enabled","wmp/IWMPPlayer::get_enabled"]
old-location: wmp\iwmpplayer_get_enabled.htm
tech.root: WMP
ms.assetid: 42dc1774-686c-4336-9a61-b658a75ba257
ms.date: 12/05/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],get_enabled method, IWMPPlayer.get_enabled, IWMPPlayer::get_enabled, IWMPPlayerget_enabled, get_enabled, get_enabled method [Windows Media Player], get_enabled method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_get_enabled, wmp/IWMPPlayer::get_enabled
f1_keywords:
- wmp/IWMPPlayer.get_enabled
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
- IWMPPlayer.get_enabled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer::get_enabled


## -description



The <b>get_enabled</b> method retrieves a value indicating whether the Windows Media Player control is enabled.




## -parameters




### -param pbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the Windows Media Player control is enabled.


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



If the <b>VARIANT_BOOL</b> received from <b>get_enabled</b> equals <b>FALSE</b>, then Windows Media Player hides the user controls during full-screen playback.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enablecontextmenu">IWMPPlayer::get_enableContextMenu</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_enabled">IWMPPlayer::put_enabled</a>
 

 

