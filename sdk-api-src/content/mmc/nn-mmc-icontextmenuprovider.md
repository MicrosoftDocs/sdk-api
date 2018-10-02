---
UID: NN:mmc.IContextMenuProvider
title: IContextMenuProvider
author: windows-sdk-content
description: The IContextMenuProvider interface implements methods that create new context menus, for the purpose of adding items to those menus, to enable extensions to extend those menus, and to display the resulting context menus.
old-location: mmc\icontextmenuprovider.htm
tech.root: MMC
ms.assetid: 3f9a5945-9b34-41fe-9c91-c782eb7eb739
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IContextMenuProvider, IContextMenuProvider interface [MMC], IContextMenuProvider interface [MMC],described, _slate_icontextmenuprovider, mmc.icontextmenuprovider, mmc/IContextMenuProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextMenuProvider interface


## -description


The 
<b>IContextMenuProvider</b> interface implements methods that create new context menus, for the purpose of adding items to those menus, to enable extensions to extend those menus, and to display the resulting context menus.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenuProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContextMenuProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/122734bd-0263-4e03-8e39-45d46c099273">AddItem</a>
</td>
<td align="left" width="63%">
Adds one item to the context menu.

(Inherited from <a href="https://msdn.microsoft.com/7186f201-13aa-4357-9b89-b435d244229c">IContextMenuCallback</a>.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/423106cd-3e81-4c4b-b28a-f7abc3bfe38b">AddPrimaryExtensionItems</a>
</td>
<td align="left" width="63%">
Enables a specified snap-in to extend the context menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8974b463-d4b6-464d-9bea-8d482d4804f3">AddThirdPartyExtensionItems</a>
</td>
<td align="left" width="63%">
Enables all snap-ins that have registered as third-party context menu extensions for this node type to extend the context menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8867d95-4812-499b-81cd-d0f9471fe33b">EmptyMenuList</a>
</td>
<td align="left" width="63%">
Clears the context menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fe9f474-c47b-4b53-8cbc-d658c82d7591">ShowContextMenu</a>
</td>
<td align="left" width="63%">
Displays the context menu.

</td>
</tr>
</table> 

