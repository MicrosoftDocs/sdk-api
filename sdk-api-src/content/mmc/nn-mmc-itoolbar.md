---
UID: NN:mmc.IToolbar
title: IToolbar (mmc.h)
description: The IToolbar interface is used to create new toolbars, to add items to them, to extend the toolbars, and to display the resultant new toolbars. Each toolbar is created on its own band within the control bar.
helpviewer_keywords: ["IToolbar","IToolbar interface [MMC]","IToolbar interface [MMC]","described","_slate_itoolbar","mmc.itoolbar","mmc/IToolbar"]
old-location: mmc\itoolbar.htm
tech.root: mmc
ms.assetid: cf9c9fe9-f58f-47f0-9051-86a514df0c6d
ms.date: 12/05/2018
ms.keywords: IToolbar, IToolbar interface [MMC], IToolbar interface [MMC],described, _slate_itoolbar, mmc.itoolbar, mmc/IToolbar
f1_keywords:
- mmc/IToolbar
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
- IToolbar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IToolbar interface


## -description


The 
<b>IToolbar</b> interface is used to create new toolbars, to add items to them, to extend the toolbars, and to display the resultant new toolbars. Each toolbar is created on its own band within the control bar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToolbar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IToolbar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IToolbar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-addbitmap">AddBitmap</a>
</td>
<td align="left" width="63%">
Adds an image to the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-addbuttons">AddButtons</a>
</td>
<td align="left" width="63%">
Adds an array of buttons to the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-deletebutton">DeleteButton</a>
</td>
<td align="left" width="63%">
Removes a button from the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-getbuttonstate">GetButtonState</a>
</td>
<td align="left" width="63%">
Gets an attribute of a button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-insertbutton">InsertButton</a>
</td>
<td align="left" width="63%">
Adds a single button to the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-setbuttonstate">SetButtonState</a>
</td>
<td align="left" width="63%">
Sets an attribute of a button.

</td>
</tr>
</table> 

