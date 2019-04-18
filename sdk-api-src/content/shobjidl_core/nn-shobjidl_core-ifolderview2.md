---
UID: NN:shobjidl_core.IFolderView2
title: IFolderView2 (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.
old-location: shell\IFolderView2.htm
tech.root: shell
ms.assetid: 52fcf0df-f532-4114-b1c9-96838f1a5e77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFolderView2, IFolderView2 interface [Windows Shell], IFolderView2 interface [Windows Shell],described, _shell_IFolderView2, shell.IFolderView2, shobjidl_core/IFolderView2
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
 - IFolderView2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView2 interface


## -description


Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderView2</b> interface inherits from <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>. <b>IFolderView2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/194804bc-c446-491b-9452-996132a65fcf">DoRename</a>
</td>
<td align="left" width="63%">
Starts a rename operation on the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/334d93c7-79a5-46c0-9042-400504aa2706">GetCurrentFolderFlags</a>
</td>
<td align="left" width="63%">
Gets the currently applied folder flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fabf321-34af-4a5e-b2c0-9ed344e1c782">GetGroupBy</a>
</td>
<td align="left" width="63%">
Retrieves the property and sort order used for grouping items in the folder display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f377b9ec-6421-454f-b2d0-f3d1b537e2c3">GetGroupSubsetCount</a>
</td>
<td align="left" width="63%">
Gets the count of visible rows displayed for a group's subset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/557ff412-2da9-4723-9f84-802e084ebaca">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents a specified item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fca9fd45-05ce-4300-aecf-a2843614a11d">GetSelectedItem</a>
</td>
<td align="left" width="63%">
Locates the currently selected item at or after a given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8ff0c8f-9678-455b-b7ec-9b651df769bc">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the current selection as an IShellItemArray.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc446188-c7f8-4158-a5b4-631fb374e0c4">GetSelectionState</a>
</td>
<td align="left" width="63%">
Gets the selection state including check state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26590565-f992-4f14-bbbc-4099a1a3ac11">GetSortColumnCount</a>
</td>
<td align="left" width="63%">
Gets the count of sort columns currently applied to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33d005bd-3ea0-42d0-ae87-417fb7c087d4">GetSortColumns</a>
</td>
<td align="left" width="63%">
Gets the sort columns currently applied to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4696d55e-aad7-41f2-b2c0-47d4b507c70c">GetViewModeAndIconSize</a>
</td>
<td align="left" width="63%">
Gets the current view mode and icon size applied to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26749aa8-9c5d-4b6b-b5af-bf52d4e8c8ce">GetViewProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for a given property key from the view's cache.
	
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b196377-53c4-49a1-be35-39d34b1638e3">GetVisibleItem</a>
</td>
<td align="left" width="63%">
Gets the next visible item in relation to a given index in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/085a08f9-c6a2-417c-973a-d0df84d8c821">InvokeVerbOnSelection</a>
</td>
<td align="left" width="63%">
Invokes the given verb on the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1687a162-f81c-422b-afc2-0b5b8b6951ad">IsMoveInSameFolder</a>
</td>
<td align="left" width="63%">
Checks to see if this view sourced the current drag-and-drop or cut-and-paste operation (used by drop target objects).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94999ac7-c9dd-439e-8f63-eeb226763200">SetCurrentFolderFlags</a>
</td>
<td align="left" width="63%">
Sets and applies specified folder flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efb2eb1a-47fa-45b2-8d8d-fc75bbe46c80">SetExtendedTileViewProperties</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d0761cb-7c81-48f7-994d-6dd61062d848">SetGroupBy</a>
</td>
<td align="left" width="63%">
Groups the view by the given property key and direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5aacc63a-d129-4539-a43f-f4dd74ab4fea">SetGroupSubsetCount</a>
</td>
<td align="left" width="63%">
Turns on group subsetting and sets the number of visible rows of items in each group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/870a72e2-25fc-421f-bd46-961bf71981cc">SetRedraw</a>
</td>
<td align="left" width="63%">
Sets redraw on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54dfac6b-8355-4064-9f54-4172975b8028">SetSortColumns</a>
</td>
<td align="left" width="63%">
Sets and sorts the view by the given sort columns.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72528831-ec5d-417e-94dd-7345b5fd7de6">SetText</a>
</td>
<td align="left" width="63%">
Sets the default text to be used when there are no items in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44abbbbb-8d4d-4a09-9c17-a2255467de44">SetTileViewProperties</a>
</td>
<td align="left" width="63%">
Set the list of tile properties for an item.
        
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52724e5d-074f-4715-9dca-50ed22d8519e">SetViewModeAndIconSize</a>
</td>
<td align="left" width="63%">
Sets and applies the view mode and image size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76d91df0-8c90-45dc-9637-910b0874e9fa">SetViewProperty</a>
</td>
<td align="left" width="63%">
Caches a property for an item in the view's property cache.
        
            

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a> interface, from which it inherits.



