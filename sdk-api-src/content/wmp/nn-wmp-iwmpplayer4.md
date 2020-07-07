---
UID: NN:wmp.IWMPPlayer4
title: IWMPPlayer4 (wmp.h)
description: The IWMPPlayer4 interface provides methods for modifying the basic behavior of the Windows Media Player control user interface.
helpviewer_keywords: ["IWMPPlayer4","IWMPPlayer4 interface [Windows Media Player]","IWMPPlayer4 interface [Windows Media Player]","described","IWMPPlayer4Interface","wmp.iwmpplayer4","wmp/IWMPPlayer4"]
old-location: wmp\iwmpplayer4.htm
tech.root: WMP
ms.assetid: afe5dbd1-96e1-4abe-b843-ec6130fa02d0
ms.date: 12/05/2018
ms.keywords: IWMPPlayer4, IWMPPlayer4 interface [Windows Media Player], IWMPPlayer4 interface [Windows Media Player],described, IWMPPlayer4Interface, wmp.iwmpplayer4, wmp/IWMPPlayer4
f1_keywords:
- wmp/IWMPPlayer4
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
- IWMPPlayer4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer4 interface


## -description



The <b>IWMPPlayer4</b> interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the <b>IWMPCore3</b> interface.

The <b>IWMPPlayer4</b> interface duplicates the methods of <b>IWMPPlayer</b>, <b>IWMPPlayer2</b>, and <b>IWMPPlayer3</b>, inherits the methods of <b>IWMPCore3</b>, and exposes the following additional methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer4</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPPlayer4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayer4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote">get_isRemote</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control is running in remote mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication">get_playerApplication</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlayerApplication</b> interface when a remoted Windows Media Player control is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-openplayer">openPlayer</a>
</td>
<td align="left" width="63%">
Opens Windows Media Player using the specified URL.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer4</b> interface either by calling the <b>QueryInterface</b> method of the <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer</a> interface or by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer2">IWMPPlayer2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer3">IWMPPlayer3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication">IWMPPlayerApplication Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

