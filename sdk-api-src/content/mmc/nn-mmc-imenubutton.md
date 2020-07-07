---
UID: NN:mmc.IMenuButton
title: IMenuButton (mmc.h)
description: The IMenuButton interface enables the user to add and manage menu buttons for a snap-in.
helpviewer_keywords: ["IMenuButton","IMenuButton interface [MMC]","IMenuButton interface [MMC]","described","_slate_imenubutton","mmc.imenubutton","mmc/IMenuButton"]
old-location: mmc\imenubutton.htm
tech.root: mmc
ms.assetid: 51bbd98a-7017-497a-858a-dd63cefc679a
ms.date: 12/05/2018
ms.keywords: IMenuButton, IMenuButton interface [MMC], IMenuButton interface [MMC],described, _slate_imenubutton, mmc.imenubutton, mmc/IMenuButton
f1_keywords:
- mmc/IMenuButton
dev_langs:
- c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmcndmgr.dll
api_name:
- IMenuButton
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMenuButton interface


## -description


The 
<b>IMenuButton</b> interface enables the user to add and manage menu buttons for a snap-in. MMC provides one menu bar per view; when a snap-in has the focus you can add one or more menu buttons for the view to this bar. These buttons are always added by appending them to the buttons already in the menu bar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuButton</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMenuButton</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuButton</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imenubutton-addbutton">AddButton</a>
</td>
<td align="left" width="63%">
Adds a button to the menu bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imenubutton-setbutton">SetButton</a>
</td>
<td align="left" width="63%">
Sets the attributes of a menu bar button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imenubutton-setbuttonstate">SetButtonState</a>
</td>
<td align="left" width="63%">
Sets the state of a menu bar button.

</td>
</tr>
</table> 

