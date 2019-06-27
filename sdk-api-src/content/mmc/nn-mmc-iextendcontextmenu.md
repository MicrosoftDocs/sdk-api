---
UID: NN:mmc.IExtendContextMenu
title: IExtendContextMenu (mmc.h)
author: windows-sdk-content
description: The IExtendContextMenu interface enables a snap-in to add items to an existing context menu.
old-location: mmc\iextendcontextmenu.htm
tech.root: mmc
ms.assetid: 8fa4434e-ccdc-43fb-877e-a6f6a5fc95b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExtendContextMenu, IExtendContextMenu interface [MMC], IExtendContextMenu interface [MMC],described, _slate_iextendcontextmenu, mmc.iextendcontextmenu, mmc/IExtendContextMenu
ms.topic: interface
f1_keywords: 
 - "mmc/IExtendContextMenu"
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendContextMenu interface


## -description


The 
<b>IExtendContextMenu</b> interface enables a snap-in to add items to an existing context menu. This is how extensions add menu items to the context menus for the objects that they insert into the scope pane or list view result pane. This interface is also the means by which third-party context menu extensions add items to the context menus of node types that they extend.

When a user right-clicks items that belong to a snap-in and are also in the scope pane or list view result pane, MMC generates a default context menu. The snap-in that added the item is offered an opportunity to extend the context menu as a primary extension. MMC then offers all registered and enabled extensions the opportunity to add additional menu items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendContextMenu</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtendContextMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendContextMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems">AddMenuItems</a>
</td>
<td align="left" width="63%">
Enables the extension to add menu items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-command">Command</a>
</td>
<td align="left" width="63%">
Indicates that an extension item on a context menu was selected.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/working-with-context-menus">Working with Context Menus</a>
 

 

