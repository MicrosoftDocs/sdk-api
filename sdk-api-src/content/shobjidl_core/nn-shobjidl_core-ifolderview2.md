---
UID: NN:shobjidl_core.IFolderView2
title: IFolderView2 (shobjidl_core.h)
description: Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.helpviewer_keywords: ["IFolderView2","IFolderView2 interface [Windows Shell]","IFolderView2 interface [Windows Shell]","described","_shell_IFolderView2","shell.IFolderView2","shobjidl_core/IFolderView2"]
old-location: shell\IFolderView2.htm
tech.root: shell
ms.assetid: 52fcf0df-f532-4114-b1c9-96838f1a5e77
ms.date: 12/05/2018
ms.keywords: IFolderView2, IFolderView2 interface [Windows Shell], IFolderView2 interface [Windows Shell],described, _shell_IFolderView2, shell.IFolderView2, shobjidl_core/IFolderView2
f1_keywords:
- shobjidl_core/IFolderView2
dev_langs:
- c++
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
- IFolderView2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView2 interface


## -description


Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderView2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>. <b>IFolderView2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderView2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-dorename">DoRename</a>
</td>
<td align="left" width="63%">
Starts a rename operation on the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getcurrentfolderflags">GetCurrentFolderFlags</a>
</td>
<td align="left" width="63%">
Gets the currently applied folder flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getgroupby">GetGroupBy</a>
</td>
<td align="left" width="63%">
Retrieves the property and sort order used for grouping items in the folder display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getgroupsubsetcount">GetGroupSubsetCount</a>
</td>
<td align="left" width="63%">
Gets the count of visible rows displayed for a group's subset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents a specified item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getselecteditem">GetSelectedItem</a>
</td>
<td align="left" width="63%">
Locates the currently selected item at or after a given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the current selection as an IShellItemArray.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getselectionstate">GetSelectionState</a>
</td>
<td align="left" width="63%">
Gets the selection state including check state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getsortcolumncount">GetSortColumnCount</a>
</td>
<td align="left" width="63%">
Gets the count of sort columns currently applied to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getsortcolumns">GetSortColumns</a>
</td>
<td align="left" width="63%">
Gets the sort columns currently applied to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getviewmodeandiconsize">GetViewModeAndIconSize</a>
</td>
<td align="left" width="63%">
Gets the current view mode and icon size applied to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getviewproperty">GetViewProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for a given property key from the view's cache.
	
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getvisibleitem">GetVisibleItem</a>
</td>
<td align="left" width="63%">
Gets the next visible item in relation to a given index in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-invokeverbonselection">InvokeVerbOnSelection</a>
</td>
<td align="left" width="63%">
Invokes the given verb on the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-ismoveinsamefolder">IsMoveInSameFolder</a>
</td>
<td align="left" width="63%">
Checks to see if this view sourced the current drag-and-drop or cut-and-paste operation (used by drop target objects).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setcurrentfolderflags">SetCurrentFolderFlags</a>
</td>
<td align="left" width="63%">
Sets and applies specified folder flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setextendedtileviewproperties">SetExtendedTileViewProperties</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setgroupby">SetGroupBy</a>
</td>
<td align="left" width="63%">
Groups the view by the given property key and direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setgroupsubsetcount">SetGroupSubsetCount</a>
</td>
<td align="left" width="63%">
Turns on group subsetting and sets the number of visible rows of items in each group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setredraw">SetRedraw</a>
</td>
<td align="left" width="63%">
Sets redraw on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setsortcolumns">SetSortColumns</a>
</td>
<td align="left" width="63%">
Sets and sorts the view by the given sort columns.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-settext">SetText</a>
</td>
<td align="left" width="63%">
Sets the default text to be used when there are no items in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-settileviewproperties">SetTileViewProperties</a>
</td>
<td align="left" width="63%">
Set the list of tile properties for an item.
        
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setviewmodeandiconsize">SetViewModeAndIconSize</a>
</td>
<td align="left" width="63%">
Sets and applies the view mode and image size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setviewproperty">SetViewProperty</a>
</td>
<td align="left" width="63%">
Caches a property for an item in the view's property cache.
        
            

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a> interface, from which it inherits.



