---
UID: NN:shobjidl_core.IShellItemArray
title: IShellItemArray
author: windows-sdk-content
description: Exposes methods that create and manipulate Shell item arrays.
old-location: shell\IShellItemArray.htm
old-project: shell
ms.assetid: 348213d1-c03f-4c38-9d13-3b1009d94e07
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IShellItemArray, IShellItemArray interface [Windows Shell], IShellItemArray interface [Windows Shell],described, _shell_IShellItemArray, shell.IShellItemArray, shobjidl_core/IShellItemArray
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItemArray interface


## -description


Exposes methods that create and manipulate <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> arrays.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemArray</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellItemArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItemArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7632d876-c00b-4dfc-862b-9a68f01bd8da">BindToHandler</a>
</td>
<td align="left" width="63%">
Binds to an object by means of the specified handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8ee210c-dab9-4678-9c62-d06677cbb395">EnumItems</a>
</td>
<td align="left" width="63%">
Gets an enumerator of the items in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0498ce03-9949-48bb-a1eb-b569f4171884">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets the attributes of the set of items contained in an <b>IShellItemArray</b>. If the array contains more than one item, the attributes retrieved by this method are not the attributes of single items, but a logical combination of all of the requested attributes of all of the items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the given <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58307102-1ae3-4249-81e0-25c1166500d0">GetItemAt</a>
</td>
<td align="left" width="63%">
Gets the item at the given index in the <b>IShellItemArray</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abedf6a4-dfad-4add-8464-571542b068cb">GetPropertyDescriptionList</a>
</td>
<td align="left" width="63%">
Gets a property description list for the items in the shell item array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/138a604f-e8dd-48ee-9678-a0530c1a16f2">GetPropertyStore</a>
</td>
<td align="left" width="63%">
Gets a property store.

</td>
</tr>
</table> 


## -remarks




            A shell item array may be created using one of the following functions:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/024ccbc7-97f1-4cb5-8588-9c9b1f747336">SHCreateShellItemArray</a>
</li>
<li>
<a href="https://msdn.microsoft.com/91e65c9a-0600-42e3-97f5-2a5960e1ec89">SHCreateShellItemArrayFromDataObject</a>
</li>
<li>
<a href="https://msdn.microsoft.com/af462941-8c23-4f48-baf5-1ead9739a2c5">SHCreateShellItemArrayFromIDLists</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93401708-6f11-474d-8009-24554f316e79">SHCreateShellItemArrayFromShellItem</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

