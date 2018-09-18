---
UID: NN:shobjidl_core.IRelatedItem
title: IRelatedItem
author: windows-sdk-content
description: Exposes methods that derive related items with specific relationships.
old-location: shell\IRelatedItem.htm
tech.root: shell
ms.assetid: f42d218c-0251-45e0-b05a-f1ccdcaf036c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IRelatedItem, IRelatedItem interface [Windows Shell], IRelatedItem interface [Windows Shell],described, _shell_IRelatedItem, shell.IRelatedItem, shobjidl_core/IRelatedItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IRelatedItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRelatedItem interface


## -description


Exposes methods that derive related items with specific relationships.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRelatedItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRelatedItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRelatedItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4aaf0016-1a0d-49ef-a001-bc4a7fe90758">GetItem</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that is related to this item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cef7dcb-be66-492c-a217-8b24d9f79506">GetItemIDList</a>
</td>
<td align="left" width="63%">
Gets the PIDL for the item that is related.

</td>
</tr>
</table> 


## -remarks



Do not implement this interface directly. This is a base interface (other interfaces derive from it) for a set of interfaces that describes the relationship between two items, (For example <a href="https://msdn.microsoft.com/78e06db0-9440-4578-bc17-96444946432a">IDisplayItem</a>).  Do not query for this interface directly, for example, using <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> or <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a>. Instead, use the derived interfaces.

An example derivation is the creation of an identity name handler. For more information, see <a href="https://msdn.microsoft.com/9e75141d-b54a-4fe8-9209-40aa7f484d24">IIdentityName</a>. Other interfaces that may derive from this interface include <a href="https://msdn.microsoft.com/a5ff7199-134d-4c1a-91e0-a81ff474f5a6">ICurrentItem</a>, and <a href="https://msdn.microsoft.com/28b4397c-dcb1-4c81-b6a3-d6abd7f7ad24">ITransferMediumItem</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a>



<a href="https://msdn.microsoft.com/fadd70cd-5018-4b71-af7b-d9c780ebddc5">IShellItem::BindToHandler</a>
 

 

