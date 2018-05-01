---
UID: NN:wiamindr_lh.IWiaDrvItem
title: IWiaDrvItem
author: windows-driver-content
description: The IWiaDrvItem interface provides methods that a WIA minidriver can use to manage a tree of IWiaDrvItem items.
old-location: image\iwiadrvitem_interface.htm
old-project: image
ms.assetid: 0609e1b2-48df-413c-90bd-d7ddea26510a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_9dbe78e4-0823-4edc-b86e-75e25d4de981.xml, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], IWiaDrvItem interface [Imaging Devices], described, image.iwiadrvitem_interface, wiamindr_lh/IWiaDrvItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wiamindr_lh.h
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
req.typenames: SCANWINDOW, *PSCANWINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wiamindr_lh.h
api_name:
-	IWiaDrvItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem interface


## -description


The <b>IWiaDrvItem</b> interface provides methods that a WIA minidriver can use to manage a tree of <b>IWiaDrvItem</b> items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaDrvItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaDrvItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaDrvItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f1cd0bf-13ce-49bc-a48e-dc3d89f3c7d7">AddItemToFolder</a>
</td>
<td align="left" width="63%">
The AddItemToFolder method adds an IWiaDrvItem item to a folder in a driver item tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e17da654-60a7-4942-99f9-f55df87a1ca3">DumpItemData</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::DumpItemData</b> method dumps private data associated with an <b>IWiaDrvItem</b> item into an allocated private buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04f446f2-cd59-4191-be0c-60140ecee3b2">FindChildItemByName</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::FindChildItemByName</b> method searches the driver item tree for a specific child item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59a77753-1f34-4224-af11-c6bbfa847619">FindItemByName</a>
</td>
<td align="left" width="63%">
The<b> IWiaDrvItem::FindItemByName</b> method locates an item in a driver item tree by the item's full name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04f8d7ef-43c6-43b7-afa1-06ae379a8e26">GetDeviceSpecContext</a>
</td>
<td align="left" width="63%">
The<b> IWiaDrvItem::GetDeviceSpecContext</b> method gets a device-specific context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e580a57-03cb-4ff4-b3c6-0b5ef17b4ccb">GetFirstChildItem</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::GetFirstChildItem</b> method gets the first child item in an <b>IWiaDrvItem</b> folder item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/810faf49-faa9-45f2-af94-af576f4c1075">GetFullItemName</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::GetFullItemName</b> method gets the item's full name, including path information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47358d69-ef45-4cac-8187-72c354912c4e">GetItemFlags</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::GetItemFlags</b> method gets the item flags of the current <b>IWiaDrvItem</b> item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e731975-13f8-4b5d-93de-714f62e9591f">GetItemName</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::GetItemName</b> method gets the current <b>IWiaDrvItem</b> item name, not including path information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc348f40-aaa4-4cd4-9dee-c02748d7412c">GetNextSiblingItem</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::GetNextSiblingItem</b> method gets the next sibling of the current item in an <b>IWiaDrvItem</b> folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6197993-b998-424e-ab5d-a91a57c7398c">GetParentItem</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::GetParentItem</b> gets the parent item of the current item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f800427e-d6b6-4f4c-aee7-4b2b0d0aa0c4">RemoveItemFromFolder</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::RemoveItemFromFolder</b> method removes an item from a parent folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6fb2929-177b-44cd-a313-8620ba9b2907">UnlinkItemTree</a>
</td>
<td align="left" width="63%">
The <b>IWiaDrvItem::UnlinkItemTree</b> method unlinks the driver item tree and releases all items in the tree.

</td>
</tr>
</table> 

