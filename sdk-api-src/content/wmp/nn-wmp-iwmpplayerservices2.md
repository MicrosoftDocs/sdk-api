---
UID: NN:wmp.IWMPPlayerServices2
title: IWMPPlayerServices2 (wmp.h)
description: The IWMPPlayerServices2 interface provides a method used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player.
helpviewer_keywords: ["IWMPPlayerServices2","IWMPPlayerServices2 interface [Windows Media Player]","IWMPPlayerServices2 interface [Windows Media Player]","described","IWMPPlayerServices2Interface","wmp.iwmpplayerservices2","wmp/IWMPPlayerServices2"]
old-location: wmp\iwmpplayerservices2.htm
tech.root: WMP
ms.assetid: abbce425-9185-4235-8d8e-28be591be8e5
ms.date: 12/05/2018
ms.keywords: IWMPPlayerServices2, IWMPPlayerServices2 interface [Windows Media Player], IWMPPlayerServices2 interface [Windows Media Player],described, IWMPPlayerServices2Interface, wmp.iwmpplayerservices2, wmp/IWMPPlayerServices2
f1_keywords:
- wmp/IWMPPlayerServices2
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
- IWMPPlayerServices2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayerServices2 interface


## -description



The <b>IWMPPlayerServices2</b> interface provides a method used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. In addition to the methods inherited from <b>IWMPPlayerServices</b>, the <b>IWMPPlayerServices2</b> interface exposes the following methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerServices2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2">IWMPPlayerServices2</a>. <b>IWMPPlayerServices2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayerServices2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices2-setbackgroundprocessingpriority">setBackgroundProcessingPriority</a>
</td>
<td align="left" width="63%">
Specifies a priority level for general background processing tasks.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayerServices2</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices">IWMPPlayerServices Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2">IWMPPlayerServices2</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

