---
UID: NN:shobjidl_core.IColumnManager
title: IColumnManager (shobjidl_core.h)
description: Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view. Each column is referenced by a PROPERTYKEY structure, which names a property.
old-location: shell\IColumnManager.htm
tech.root: shell
ms.assetid: d01cacd8-1867-4f44-bbc3-876bd727c0fe
ms.date: 12/05/2018
ms.keywords: IColumnManager, IColumnManager interface [Windows Shell], IColumnManager interface [Windows Shell],described, shell.IColumnManager, shell_IColumnManager, shobjidl_core/IColumnManager
f1_keywords:
- shobjidl_core/IColumnManager
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IColumnManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IColumnManager interface


## -description


Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view. Each column is referenced by a <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure, which names a property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IColumnManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IColumnManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IColumnManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-getcolumncount">GetColumnCount</a>
</td>
<td align="left" width="63%">
Gets the column count for either the visible columns or the complete set of columns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-getcolumninfo">GetColumnInfo</a>
</td>
<td align="left" width="63%">
Gets information about each column: width, visibility, display name, and state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-getcolumns">GetColumns</a>
</td>
<td align="left" width="63%">
Gets an array of <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures that represent the columns that the view supports. Includes either all columns or only those currently visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo">SetColumnInfo</a>
</td>
<td align="left" width="63%">
Sets the state for a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumns">SetColumns</a>
</td>
<td align="left" width="63%">
Sets the collection of columns for the view to display.

</td>
</tr>
</table> 


## -remarks



This interface can be accessed even when the Windows Explorer window is in a non-column view mode such as icons, thumbnails, or tiles. It affects those views, as well as views in which the column header control displays the set of columns to which <b>IColumnManager</b> provides access.

The default implementation of the Windows Explorer view object, created by <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>, supports this interface retrieved through <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a>. Code that runs in the Windows Explorer (such as view callbacks, context menus or drop targets) can access the view object using <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a>, querying for <b>SID_SFolderView</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a>
 

 

