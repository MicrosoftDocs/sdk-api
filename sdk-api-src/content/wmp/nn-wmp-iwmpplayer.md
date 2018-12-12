---
UID: NN:wmp.IWMPPlayer
title: IWMPPlayer
author: windows-sdk-content
description: The IWMPPlayer interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the IWMPCore interface.
old-location: wmp\iwmpplayer.htm
tech.root: WMP
ms.assetid: ce6aef79-1faa-44ac-a096-f65d09458067
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlayer, IWMPPlayer interface [Windows Media Player], IWMPPlayer interface [Windows Media Player],described, IWMPPlayerInterface, wmp.iwmpplayer, wmp/IWMPPlayer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IWMPPlayer interface


## -description



The <b>IWMPPlayer</b> interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the <b>IWMPCore</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore</a>. <b>IWMPPlayer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563539(v=VS.85).aspx">get_enableContextMenu</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563540(v=VS.85).aspx">get_enabled</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563541(v=VS.85).aspx">get_fullScreen</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video content is played back in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563542(v=VS.85).aspx">get_uiMode</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating which controls are shown in the user interface when Windows Media Player is embedded in a webpage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563543(v=VS.85).aspx">put_enableContextMenu</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563544(v=VS.85).aspx">put_enabled</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether the Windows Media Player control is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563545(v=VS.85).aspx">put_fullScreen</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether video content is played back in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563546(v=VS.85).aspx">put_uiMode</a>
</td>
<td align="left" width="63%">
Specifies a value indicating which controls are shown in the user interface when Windows Media Player is embedded in a webpage.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563217(v=VS.85).aspx">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563219(v=VS.85).aspx">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563515(v=VS.85).aspx">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563521(v=VS.85).aspx">IWMPPlayer3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563522(v=VS.85).aspx">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

