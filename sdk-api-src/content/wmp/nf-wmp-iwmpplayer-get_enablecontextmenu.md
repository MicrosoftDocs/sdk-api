---
UID: NF:wmp.IWMPPlayer.get_enableContextMenu
title: IWMPPlayer::get_enableContextMenu
author: windows-sdk-content
description: The get_enableContextMenu method retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.
old-location: wmp\iwmpplayer_get_enablecontextmenu.htm
old-project: WMP
ms.assetid: 66769441-7923-45d2-b84f-24770537923c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],get_enableContextMenu method, IWMPPlayer.get_enableContextMenu, IWMPPlayer::get_enableContextMenu, IWMPPlayerget_enableContextMenu, get_enableContextMenu, get_enableContextMenu method [Windows Media Player], get_enableContextMenu method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_get_enablecontextmenu, wmp/IWMPPlayer::get_enableContextMenu
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlayer.get_enableContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/42dc1774-686c-4336-9a61-b658a75ba257">IWMPPlayer::get_enabled</a>



<a href="https://msdn.microsoft.com/8e05342f-812a-4dca-a491-b237f9a9f1bd">IWMPPlayer::get_uiMode</a>



<a href="https://msdn.microsoft.com/1fd79fc3-34c6-4d76-a726-bbf64ee983c9">IWMPPlayer::put_enableContextMenu</a>
 

 

