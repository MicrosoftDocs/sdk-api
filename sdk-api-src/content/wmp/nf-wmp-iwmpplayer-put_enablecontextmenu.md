---
UID: NF:wmp.IWMPPlayer.put_enableContextMenu
title: IWMPPlayer::put_enableContextMenu
author: windows-sdk-content
description: The put_enableContextMenu method specifies a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.
old-location: wmp\iwmpplayer_put_enablecontextmenu.htm
tech.root: WMP
ms.assetid: 1fd79fc3-34c6-4d76-a726-bbf64ee983c9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],put_enableContextMenu method, IWMPPlayer.put_enableContextMenu, IWMPPlayer::put_enableContextMenu, IWMPPlayerput_enableContextMenu, put_enableContextMenu, put_enableContextMenu method [Windows Media Player], put_enableContextMenu method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_put_enablecontextmenu, wmp/IWMPPlayer::put_enableContextMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWMPPlayer.put_enableContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayer::put_enableContextMenu


## -description



The <b>put_enableContextMenu</b> method specifies a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.




## -parameters




### -param bEnableContextMenu [in]

<b>VARIANT_BOOL</b> that indicates whether to the enable context menu. The default is <b>TRUE</b>.


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



During full-screen playback, Windows Media Player hides the mouse cursor when the <b>VARIANT_BOOL</b> retrieved by <b>IWMPPlayer::get_enableContextMenu</b> equals <b>FALSE</b> and the <b>BSTR</b> retrieved by <b>IWMPPlayer::get_uiMode</b> equals "none".

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/66769441-7923-45d2-b84f-24770537923c">IWMPPlayer::get_enableContextMenu</a>



<a href="https://msdn.microsoft.com/8e05342f-812a-4dca-a491-b237f9a9f1bd">IWMPPlayer::get_uiMode</a>



<a href="https://msdn.microsoft.com/c0e29724-1689-4b59-a9bd-b9cc3f391b68">IWMPPlayer::put_enabled</a>
 

 

