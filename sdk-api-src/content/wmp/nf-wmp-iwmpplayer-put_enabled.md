---
UID: NF:wmp.IWMPPlayer.put_enabled
title: IWMPPlayer::put_enabled
author: windows-sdk-content
description: The put_enabled method specifies a value indicating whether the Windows Media Player control is enabled.
old-location: wmp\iwmpplayer_put_enabled.htm
old-project: WMP
ms.assetid: c0e29724-1689-4b59-a9bd-b9cc3f391b68
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],put_enabled method, IWMPPlayer.put_enabled, IWMPPlayer::put_enabled, IWMPPlayerput_enabled, put_enabled, put_enabled method [Windows Media Player], put_enabled method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_put_enabled, wmp/IWMPPlayer::put_enabled
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
 - IWMPPlayer.put_enabled
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayer::put_enabled


## -description



The <b>put_enabled</b> method specifies a value indicating whether the Windows Media Player control is enabled.




## -parameters




### -param bEnabled [in]

<b>VARIANT_BOOL</b> indicating whether the Windows Media Player control is enabled.


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



If the <b>VARIANT_BOOL</b> specified in <b>put_enabled</b> is set to <b>FALSE</b>, then Windows Media Player hides the user controls during full-screen playback.




## -see-also




<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/42dc1774-686c-4336-9a61-b658a75ba257">IWMPPlayer::get_enabled</a>



<a href="https://msdn.microsoft.com/1fd79fc3-34c6-4d76-a726-bbf64ee983c9">IWMPPlayer::put_enableContextMenu</a>
 

 

