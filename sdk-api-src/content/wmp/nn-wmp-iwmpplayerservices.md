---
UID: NN:wmp.IWMPPlayerServices
title: IWMPPlayerServices (wmp.h)
description: The IWMPPlayerServices interface provides methods used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. These methods can only be used with C++.
helpviewer_keywords: ["IWMPPlayerServices","IWMPPlayerServices interface [Windows Media Player]","IWMPPlayerServices interface [Windows Media Player]","described","IWMPPlayerServicesInterface","wmp.iwmpplayerservices","wmp/IWMPPlayerServices"]
old-location: wmp\iwmpplayerservices.htm
tech.root: WMP
ms.assetid: 3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e
ms.date: 12/05/2018
ms.keywords: IWMPPlayerServices, IWMPPlayerServices interface [Windows Media Player], IWMPPlayerServices interface [Windows Media Player],described, IWMPPlayerServicesInterface, wmp.iwmpplayerservices, wmp/IWMPPlayerServices
f1_keywords:
- wmp/IWMPPlayerServices
dev_langs:
- c++
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
- IWMPPlayerServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayerServices interface


## -description



The <b>IWMPPlayerServices</b> interface provides methods used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. These methods can only be used with C++.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPPlayerServices</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-activateuiplugin">activateUIPlugin</a>
</td>
<td align="left" width="63%">
Activates the specified user interface (UI) plug-in in the full mode of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane">setTaskPane</a>
</td>
<td align="left" width="63%">
Displays the specified task pane in the full mode of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpaneurl">setTaskPaneURL (deprecated)</a>
</td>
<td align="left" width="63%">
Displays the specified URL in the specified task pane of the full mode of Windows Media Player.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayerServices</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

