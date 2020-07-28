---
UID: NN:wmp.IWMPPlayerApplication
title: IWMPPlayerApplication (wmp.h)
description: The IWMPPlayerApplication interface provides methods for switching between a remoted Windows Media Player control and the full mode of the Player. These methods can only be used with C++ programs that embed the control in remote mode.
helpviewer_keywords: ["IWMPPlayerApplication","IWMPPlayerApplication interface [Windows Media Player]","IWMPPlayerApplication interface [Windows Media Player]","described","IWMPPlayerApplicationInterface","wmp.iwmpplayerapplication","wmp/IWMPPlayerApplication"]
old-location: wmp\iwmpplayerapplication.htm
tech.root: WMP
ms.assetid: bcdd7ea9-66b2-40e9-89a1-0fec073ccd92
ms.date: 12/05/2018
ms.keywords: IWMPPlayerApplication, IWMPPlayerApplication interface [Windows Media Player], IWMPPlayerApplication interface [Windows Media Player],described, IWMPPlayerApplicationInterface, wmp.iwmpplayerapplication, wmp/IWMPPlayerApplication
f1_keywords:
- wmp/IWMPPlayerApplication
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
- IWMPPlayerApplication
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayerApplication interface


## -description



The <b>IWMPPlayerApplication</b> interface provides methods for switching between a remoted Windows Media Player control and the full mode of the Player. These methods can only be used with C++ programs that embed the control in remote mode.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerApplication</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPPlayerApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayerApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay">get_hasDisplay</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video can display through the remoted Windows Media Player control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked">get_playerDocked</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether Windows Media Player is in a docked state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol">switchToControl</a>
</td>
<td align="left" width="63%">
Switches a remoted Windows Media Player control to the docked state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf5a77c5-298e-48de-80cd-d7ecd9e74323">switchToPlayerApplication</a>
</td>
<td align="left" width="63%">
Switches a remoted Windows Media Player control to the full mode of the Player..

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayerApplication</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication">get_playerApplication</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

