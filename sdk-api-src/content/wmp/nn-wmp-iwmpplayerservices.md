---
UID: NN:wmp.IWMPPlayerServices
title: IWMPPlayerServices
author: windows-driver-content
description: The IWMPPlayerServices interface provides methods used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. These methods can only be used with C++.
old-location: wmp\iwmpplayerservices.htm
old-project: WMP
ms.assetid: 3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPPlayerServices, IWMPPlayerServices interface [Windows Media Player], IWMPPlayerServices interface [Windows Media Player],described, IWMPPlayerServicesInterface, wmp.iwmpplayerservices, wmp/IWMPPlayerServices
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPPlayerServices
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayerServices interface


## -description



The <b>IWMPPlayerServices</b> interface provides methods used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. These methods can only be used with C++.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPPlayerServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayerServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73274f71-ba34-479c-a23c-38a564e950fa">activateUIPlugin</a>
</td>
<td align="left" width="63%">
Activates the specified user interface (UI) plug-in in the full mode of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b34ec95-d9a3-4135-b369-39955199ac00">setTaskPane</a>
</td>
<td align="left" width="63%">
Displays the specified task pane in the full mode of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ceacaeb-09af-4cdf-84b7-04574a83ec48">setTaskPaneURL (deprecated)</a>
</td>
<td align="left" width="63%">
Displays the specified URL in the specified task pane of the full mode of Windows Media Player.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPPlayerServices</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

