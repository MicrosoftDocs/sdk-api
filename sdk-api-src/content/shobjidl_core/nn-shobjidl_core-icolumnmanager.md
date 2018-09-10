---
UID: NN:shobjidl_core.IColumnManager
title: IColumnManager
author: windows-sdk-content
description: Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view. Each column is referenced by a PROPERTYKEY structure, which names a property.
old-location: shell\IColumnManager.htm
tech.root: shell
ms.assetid: d01cacd8-1867-4f44-bbc3-876bd727c0fe
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IColumnManager, IColumnManager interface [Windows Shell], IColumnManager interface [Windows Shell],described, shell.IColumnManager, shell_IColumnManager, shobjidl_core/IColumnManager
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IColumnManager interface


## -description


Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view. Each column is referenced by a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure, which names a property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IColumnManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IColumnManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ab01c803-860e-4a16-9ed1-4c978af5b150">GetColumnCount</a>
</td>
<td align="left" width="63%">
Gets the column count for either the visible columns or the complete set of columns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22b3e5a6-a0a1-46e4-91b8-7bfe3944fffb">GetColumnInfo</a>
</td>
<td align="left" width="63%">
Gets information about each column: width, visibility, display name, and state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/297a8e75-78a0-4bfb-83c0-0b58111dcf1c">GetColumns</a>
</td>
<td align="left" width="63%">
Gets an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures that represent the columns that the view supports. Includes either all columns or only those currently visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a52d634-0ff0-4dbc-81cb-90cdffe4f6ae">SetColumnInfo</a>
</td>
<td align="left" width="63%">
Sets the state for a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1541809d-0826-46c4-aa10-cb4cbd6f8437">SetColumns</a>
</td>
<td align="left" width="63%">
Sets the collection of columns for the view to display.

</td>
</tr>
</table> 


## -remarks



This interface can be accessed even when the Windows Explorer window is in a non-column view mode such as icons, thumbnails, or tiles. It affects those views, as well as views in which the column header control displays the set of columns to which <b>IColumnManager</b> provides access.

The default implementation of the Windows Explorer view object, created by <a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a>, supports this interface retrieved through <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>. Code that runs in the Windows Explorer (such as view callbacks, context menus or drop targets) can access the view object using <a href="_inet_IServiceProvider_QueryService_Method">IServiceProvider::QueryService</a>, querying for <b>SID_SFolderView</b>.




## -see-also




<a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a>
 

 

