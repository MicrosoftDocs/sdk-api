---
UID: NN:shobjidl_core.ISearchFolderItemFactory
title: ISearchFolderItemFactory
author: windows-sdk-content
description: Exposes methods that create and modify search folders.
old-location: shell\ISearchFolderItemFactory.htm
old-project: shell
ms.assetid: a684b373-6de4-4b4a-bbae-85e1c5a7e04a
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ISearchFolderItemFactory, ISearchFolderItemFactory interface [Windows Shell], ISearchFolderItemFactory interface [Windows Shell],described, _shell_ISearchFolderItemFactory, shell.ISearchFolderItemFactory, shobjidl_core/ISearchFolderItemFactory
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
 - ISearchFolderItemFactory
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ISearchFolderItemFactory interface


## -description


Exposes methods that create and modify search folders. The Set methods are called first to set up the parameters of the search.  When not called, default values will be used instead.  <a href="https://msdn.microsoft.com/9547c429-9396-474e-b772-6e3aa28d1937">ISearchFolderItemFactory::GetIDList</a> and <a href="https://msdn.microsoft.com/fc5dd159-8a47-479f-b087-bd161093d0a0">ISearchFolderItemFactory::GetShellItem</a> return the two forms of the search specified by these parameters.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchFolderItemFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchFolderItemFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchFolderItemFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9547c429-9396-474e-b772-6e3aa28d1937">GetIDList</a>
</td>
<td align="left" width="63%">
Gets the search folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc5dd159-8a47-479f-b087-bd161093d0a0">GetShellItem</a>
</td>
<td align="left" width="63%">
Gets the search folder as a <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ac5acc3-e522-4b6f-a31c-c0850445e00c">SetCondition</a>
</td>
<td align="left" width="63%">
Sets the  <a href="_search_ICondition">ICondition</a> of the search.  When this method is not called, the resulting search will have no filters applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2552677b-7907-4a2b-8a2f-6769bca64029">SetDisplayName</a>
</td>
<td align="left" width="63%">
Sets the search folder display name, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef72f196-cfd5-4547-85cb-0ccfdc496c46">SetFolderLogicalViewMode</a>
</td>
<td align="left" width="63%">

      Sets folder logical view mode. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://msdn.microsoft.com/a9b09dc6-751e-4d5f-b016-0b26c15c68f6">ISearchFolderItemFactory::SetFolderTypeID</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9b09dc6-751e-4d5f-b016-0b26c15c68f6">SetFolderTypeID</a>
</td>
<td align="left" width="63%">
Sets a search folder type ID, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52967ebe-3a8c-4696-aa5d-251a4cf58469">SetGroupColumn</a>
</td>
<td align="left" width="63%">
Sets a group column, as specified. If no group column is specified, no grouping occurs.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9a6650f-d9fe-43e8-aed5-9a7006883148">SetIconSize</a>
</td>
<td align="left" width="63%">
Sets the search folder icon size, as specified. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://msdn.microsoft.com/a9b09dc6-751e-4d5f-b016-0b26c15c68f6">ISearchFolderItemFactory::SetFolderTypeID</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556773">SetScope</a>
</td>
<td align="left" width="63%">
Sets search scope, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c91667fa-a48b-409a-ba96-35581fdd07dd">SetSortColumns</a>
</td>
<td align="left" width="63%">
Creates a list of sort column directions, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2f3d975-b968-4491-868f-90eccb40e8e4">SetStacks</a>
</td>
<td align="left" width="63%">
Creates a list of stack keys, as specified. If this method is not called, by default the folder will not be stacked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be18218e-a117-4256-936e-3a5eb36c3654">SetVisibleColumns</a>
</td>
<td align="left" width="63%">
Creates a new column list whose columns are all visible, given an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures.  The default is based on <b>FolderTypeID</b>.

</td>
</tr>
</table> 


## -remarks



To implement this interface use class ID <b>CLSID_SearchFolderItemFactory</b>.



