---
UID: NN:wmp.IWMPPlayer
title: IWMPPlayer
author: windows-sdk-content
description: The IWMPPlayer interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the IWMPCore interface.
old-location: wmp\iwmpplayer.htm
old-project: WMP
ms.assetid: ce6aef79-1faa-44ac-a096-f65d09458067
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPPlayer, IWMPPlayer interface [Windows Media Player], IWMPPlayer interface [Windows Media Player],described, IWMPPlayerInterface, wmp.iwmpplayer, wmp/IWMPPlayer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayer interface


## -description



The <b>IWMPPlayer</b> interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the <b>IWMPCore</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer</b> interface inherits from <a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>. <b>IWMPPlayer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/66769441-7923-45d2-b84f-24770537923c">get_enableContextMenu</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42dc1774-686c-4336-9a61-b658a75ba257">get_enabled</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a8bb0b5-76c6-424f-ba37-5e913b6ed542">get_fullScreen</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video content is played back in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e05342f-812a-4dca-a491-b237f9a9f1bd">get_uiMode</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating which controls are shown in the user interface when Windows Media Player is embedded in a webpage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fd79fc3-34c6-4d76-a726-bbf64ee983c9">put_enableContextMenu</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0e29724-1689-4b59-a9bd-b9cc3f391b68">put_enabled</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether the Windows Media Player control is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50ce0115-9e49-4431-b818-35bdc34da9a0">put_fullScreen</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether video content is played back in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/154db914-a0c3-44de-b692-e1b7f9c681f6">put_uiMode</a>
</td>
<td align="left" width="63%">
Specifies a value indicating which controls are shown in the user interface when Windows Media Player is embedded in a webpage.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/5f839bfe-bf67-49eb-8743-57713e1be7c5">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/3004551e-ce36-4f15-88c3-93b2bfaa72fc">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/bf51d54d-d0aa-42ad-8180-d1f6487baac8">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/0d8a9414-5c5c-40e0-a34c-430ead01ef26">IWMPPlayer3 Interface</a>



<a href="https://msdn.microsoft.com/afe5dbd1-96e1-4abe-b843-ec6130fa02d0">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

