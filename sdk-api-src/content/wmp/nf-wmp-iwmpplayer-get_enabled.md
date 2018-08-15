---
UID: NF:wmp.IWMPPlayer.get_enabled
title: IWMPPlayer::get_enabled
author: windows-sdk-content
description: The get_enabled method retrieves a value indicating whether the Windows Media Player control is enabled.
old-location: wmp\iwmpplayer_get_enabled.htm
old-project: WMP
ms.assetid: 42dc1774-686c-4336-9a61-b658a75ba257
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],get_enabled method, IWMPPlayer.get_enabled, IWMPPlayer::get_enabled, IWMPPlayerget_enabled, get_enabled, get_enabled method [Windows Media Player], get_enabled method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_get_enabled, wmp/IWMPPlayer::get_enabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
 - IWMPPlayer.get_enabled
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/66769441-7923-45d2-b84f-24770537923c">IWMPPlayer::get_enableContextMenu</a>



<a href="https://msdn.microsoft.com/c0e29724-1689-4b59-a9bd-b9cc3f391b68">IWMPPlayer::put_enabled</a>
 

 

