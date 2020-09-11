---
UID: NN:shobjidl_core.IShellItemArray
title: IShellItemArray (shobjidl_core.h)
description: Exposes methods that create and manipulate Shell item arrays.
helpviewer_keywords: ["IShellItemArray","IShellItemArray interface [Windows Shell]","IShellItemArray interface [Windows Shell]","described","_shell_IShellItemArray","shell.IShellItemArray","shobjidl_core/IShellItemArray"]
old-location: shell\IShellItemArray.htm
tech.root: shell
ms.assetid: 348213d1-c03f-4c38-9d13-3b1009d94e07
ms.date: 12/05/2018
ms.keywords: IShellItemArray, IShellItemArray interface [Windows Shell], IShellItemArray interface [Windows Shell],described, _shell_IShellItemArray, shell.IShellItemArray, shobjidl_core/IShellItemArray
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemArray
 - shobjidl_core/IShellItemArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray
---

# IShellItemArray interface


## -description

Exposes methods that create and manipulate <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> arrays.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemArray</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellItemArray</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-bindtohandler">BindToHandler</a>
</td>
<td align="left" width="63%">
Binds to an object by means of the specified handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-enumitems">EnumItems</a>
</td>
<td align="left" width="63%">
Gets an enumerator of the items in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets the attributes of the set of items contained in an <b>IShellItemArray</b>. If the array contains more than one item, the attributes retrieved by this method are not the attributes of single items, but a logical combination of all of the requested attributes of all of the items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the given <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getitemat">GetItemAt</a>
</td>
<td align="left" width="63%">
Gets the item at the given index in the <b>IShellItemArray</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getpropertydescriptionlist">GetPropertyDescriptionList</a>
</td>
<td align="left" width="63%">
Gets a property description list for the items in the shell item array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getpropertystore">GetPropertyStore</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray">SHCreateShellItemArray</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject">SHCreateShellItemArrayFromDataObject</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists">SHCreateShellItemArrayFromIDLists</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem">SHCreateShellItemArrayFromShellItem</a>
</li>
</ul>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>

