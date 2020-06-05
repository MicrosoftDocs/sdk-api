---
UID: NN:shobjidl_core.ISearchFolderItemFactory
title: ISearchFolderItemFactory (shobjidl_core.h)
description: Exposes methods that create and modify search folders.helpviewer_keywords: ["ISearchFolderItemFactory","ISearchFolderItemFactory interface [Windows Shell]","ISearchFolderItemFactory interface [Windows Shell]","described","_shell_ISearchFolderItemFactory","shell.ISearchFolderItemFactory","shobjidl_core/ISearchFolderItemFactory"]
old-location: shell\ISearchFolderItemFactory.htm
tech.root: shell
ms.assetid: a684b373-6de4-4b4a-bbae-85e1c5a7e04a
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory, ISearchFolderItemFactory interface [Windows Shell], ISearchFolderItemFactory interface [Windows Shell],described, _shell_ISearchFolderItemFactory, shell.ISearchFolderItemFactory, shobjidl_core/ISearchFolderItemFactory
f1_keywords:
- shobjidl_core/ISearchFolderItemFactory
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
- ISearchFolderItemFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchFolderItemFactory interface


## -description


Exposes methods that create and modify search folders. The Set methods are called first to set up the parameters of the search.  When not called, default values will be used instead.  <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist">ISearchFolderItemFactory::GetIDList</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem">ISearchFolderItemFactory::GetShellItem</a> return the two forms of the search specified by these parameters.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchFolderItemFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchFolderItemFactory</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist">GetIDList</a>
</td>
<td align="left" width="63%">
Gets the search folder as an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem">GetShellItem</a>
</td>
<td align="left" width="63%">
Gets the search folder as a <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setcondition">SetCondition</a>
</td>
<td align="left" width="63%">
Sets the  <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> of the search.  When this method is not called, the resulting search will have no filters applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setdisplayname">SetDisplayName</a>
</td>
<td align="left" width="63%">
Sets the search folder display name, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode">SetFolderLogicalViewMode</a>
</td>
<td align="left" width="63%">
Sets folder logical view mode. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfoldertypeid">ISearchFolderItemFactory::SetFolderTypeID</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfoldertypeid">SetFolderTypeID</a>
</td>
<td align="left" width="63%">
Sets a search folder type ID, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setgroupcolumn">SetGroupColumn</a>
</td>
<td align="left" width="63%">
Sets a group column, as specified. If no group column is specified, no grouping occurs.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-seticonsize">SetIconSize</a>
</td>
<td align="left" width="63%">
Sets the search folder icon size, as specified. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfoldertypeid">ISearchFolderItemFactory::SetFolderTypeID</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setscope">SetScope</a>
</td>
<td align="left" width="63%">
Sets search scope, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setsortcolumns">SetSortColumns</a>
</td>
<td align="left" width="63%">
Creates a list of sort column directions, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setstacks">SetStacks</a>
</td>
<td align="left" width="63%">
Creates a list of stack keys, as specified. If this method is not called, by default the folder will not be stacked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setvisiblecolumns">SetVisibleColumns</a>
</td>
<td align="left" width="63%">
Creates a new column list whose columns are all visible, given an array of <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures.  The default is based on <b>FolderTypeID</b>.

</td>
</tr>
</table> 


## -remarks



To implement this interface use class ID <b>CLSID_SearchFolderItemFactory</b>.



