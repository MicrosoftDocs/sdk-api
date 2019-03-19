---
UID: NN:shobjidl_core.IParentAndItem
title: IParentAndItem (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that get and set the parent and the parent's child ID. While IParentAndItem is typically implemented on IShellItems, it is not specific to IShellItem.
old-location: shell\IParentAndItem.htm
tech.root: shell
ms.assetid: 5cca426f-73fb-4b39-8eb0-16c01673c311
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IParentAndItem, IParentAndItem interface [Windows Shell], IParentAndItem interface [Windows Shell],described, _shell_IParentAndItem, shell.IParentAndItem, shobjidl_core/IParentAndItem
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
 - IParentAndItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IParentAndItem interface


## -description


Exposes methods that get and set the parent and the parent's child ID. While <b>IParentAndItem</b> is typically implemented on IShellItems, it is not specific to <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.
         


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IParentAndItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IParentAndItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IParentAndItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/351ad043-949c-46e1-a6cd-bcc15016f42a">GetParentAndItem</a>
</td>
<td align="left" width="63%">
Gets the parent of an item and the parent's child ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/398bb0c1-39f1-4a51-9382-421639ab7b8e">SetParentAndItem</a>
</td>
<td align="left" width="63%">
Sets the parent of an item and the parent's child ID.

</td>
</tr>
</table> 


## -remarks



The performance improvement using this interface can be noted in comparison with <a href="https://msdn.microsoft.com/b367dc07-8a50-4562-bd73-57c73c781d81">IPersistIDList</a>, an interface that uses absolute item identifier lists. Subsequent operations on objects that implement <b>IPersistIDList</b> may require <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a> calls, and these calls may impact performance.  In the case of IShellItems and participating IShellFolders that implement <b>IParentAndItem</b>, the parent <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> may already be cached. By implementing <b>IParentAndItem</b> and then getting/setting the parent <b>IShellFolder</b> directly, the call to <b>IShellFolder::BindToObject</b> on the item identifier list to retrieve the <b>IShellFolder</b> interface is eliminated.



