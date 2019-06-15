---
UID: NN:wmp.IWMPPlayer
title: IWMPPlayer (wmp.h)
author: windows-sdk-content
description: The IWMPPlayer interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the IWMPCore interface.
old-location: wmp\iwmpplayer.htm
tech.root: WMP
ms.assetid: ce6aef79-1faa-44ac-a096-f65d09458067
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPPlayer, IWMPPlayer interface [Windows Media Player], IWMPPlayer interface [Windows Media Player],described, IWMPPlayerInterface, wmp.iwmpplayer, wmp/IWMPPlayer
ms.topic: interface
f1_keywords: ["wmp/IWMPPlayer"]
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPPlayer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer interface


## -description



The <b>IWMPPlayer</b> interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the <b>IWMPCore</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>. <b>IWMPPlayer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enablecontextmenu">get_enableContextMenu</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enabled">get_enabled</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_fullscreen">get_fullScreen</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video content is played back in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_uimode">get_uiMode</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating which controls are shown in the user interface when Windows Media Player is embedded in a webpage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_enablecontextmenu">put_enableContextMenu</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_enabled">put_enabled</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether the Windows Media Player control is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_fullscreen">put_fullScreen</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether video content is played back in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_uimode">put_uiMode</a>
</td>
<td align="left" width="63%">
Specifies a value indicating which controls are shown in the user interface when Windows Media Player is embedded in a webpage.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer2">IWMPPlayer2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer3">IWMPPlayer3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

