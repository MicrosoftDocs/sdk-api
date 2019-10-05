---
UID: NN:mmc.IContextMenuProvider
title: IContextMenuProvider (mmc.h)
author: windows-sdk-content
description: The IContextMenuProvider interface implements methods that create new context menus, for the purpose of adding items to those menus, to enable extensions to extend those menus, and to display the resulting context menus.
old-location: mmc\icontextmenuprovider.htm
tech.root: mmc
ms.assetid: 3f9a5945-9b34-41fe-9c91-c782eb7eb739
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IContextMenuProvider, IContextMenuProvider interface [MMC], IContextMenuProvider interface [MMC],described, _slate_icontextmenuprovider, mmc.icontextmenuprovider, mmc/IContextMenuProvider
ms.topic: interface
f1_keywords: 
 - "mmc/IContextMenuProvider"
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
 - IContextMenuProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContextMenuProvider interface


## -description


The 
<b>IContextMenuProvider</b> interface implements methods that create new context menus, for the purpose of adding items to those menus, to enable extensions to extend those menus, and to display the resulting context menus.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenuProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextMenuProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenuProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814824(v=vs.85)">AddItem</a>
</td>
<td align="left" width="63%">
Adds one item to the context menu.

(Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontextmenucallback-additem">IContextMenuCallback</a>.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-addprimaryextensionitems">AddPrimaryExtensionItems</a>
</td>
<td align="left" width="63%">
Enables a specified snap-in to extend the context menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-addthirdpartyextensionitems">AddThirdPartyExtensionItems</a>
</td>
<td align="left" width="63%">
Enables all snap-ins that have registered as third-party context menu extensions for this node type to extend the context menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-emptymenulist">EmptyMenuList</a>
</td>
<td align="left" width="63%">
Clears the context menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-showcontextmenu">ShowContextMenu</a>
</td>
<td align="left" width="63%">
Displays the context menu.

</td>
</tr>
</table> 

