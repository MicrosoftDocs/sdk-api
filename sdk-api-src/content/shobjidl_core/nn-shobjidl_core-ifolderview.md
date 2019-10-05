---
UID: NN:shobjidl_core.IFolderView
title: IFolderView (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.
old-location: shell\IFolderView.htm
tech.root: shell
ms.assetid: 3bc2615e-f07c-4959-b89e-bbbd2bf45a94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFolderView, IFolderView interface [Windows Shell], IFolderView interface [Windows Shell],described, _shell_IFolderView, shell.IFolderView, shobjidl_core/IFolderView
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IFolderView"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView interface


## -description


Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderView</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFolderView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getautoarrange">GetAutoArrange</a>
</td>
<td align="left" width="63%">
Gets the current state of the folder's Auto Arrange mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getcurrentviewmode">GetCurrentViewMode</a>
</td>
<td align="left" width="63%">
Gets an address containing a value representing the folder's current view mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getdefaultspacing">GetDefaultSpacing</a>
</td>
<td align="left" width="63%">
Gets a pointer to a POINT structure containing the default width (x) and height (y) measurements of an item, including the surrounding white space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfocuseditem">GetFocusedItem</a>
</td>
<td align="left" width="63%">
Gets the index of the item that currently has focus in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder">GetFolder</a>
</td>
<td align="left" width="63%">
Gets the folder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getitemposition">GetItemPosition</a>
</td>
<td align="left" width="63%">
Gets the position of an item in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getselectionmarkeditem">GetSelectionMarkedItem</a>
</td>
<td align="left" width="63%">
Gets the index of an item in the folder's view which has been marked by using the SVSI_SELECTIONMARK in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectitem">IFolderView::SelectItem</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getspacing">GetSpacing</a>
</td>
<td align="left" width="63%">
Gets a POINT structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-item">Item</a>
</td>
<td align="left" width="63%">
Gets the identifier of a specific item in the folder view, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount">ItemCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the folder. This can be the number of all items, or a subset such as the number of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items">Items</a>
</td>
<td align="left" width="63%">
Gets the address of an enumeration object based on the collection of items in the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectandpositionitems">SelectAndPositionItems</a>
</td>
<td align="left" width="63%">
Allows the selection and positioning of items visible in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectitem">SelectItem</a>
</td>
<td align="left" width="63%">
Selects an item in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-setcurrentviewmode">SetCurrentViewMode</a>
</td>
<td align="left" width="63%">
Sets the selected folder's view mode.

</td>
</tr>
</table> 

