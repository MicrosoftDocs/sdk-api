---
UID: NN:shobjidl_core.IFolderView
title: IFolderView
author: windows-sdk-content
description: Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.
old-location: shell\IFolderView.htm
tech.root: Shell
ms.assetid: 3bc2615e-f07c-4959-b89e-bbbd2bf45a94
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IFolderView, IFolderView interface [Windows Shell], IFolderView interface [Windows Shell],described, _shell_IFolderView, shell.IFolderView, shobjidl_core/IFolderView
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView interface


## -description


Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFolderView</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/987383c8-aaea-4144-8a8c-b4a8943a2acd">GetAutoArrange</a>
</td>
<td align="left" width="63%">
Gets the current state of the folder's Auto Arrange mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8f69203-f0b4-4537-980c-8e5bbdb49aab">GetCurrentViewMode</a>
</td>
<td align="left" width="63%">
Gets an address containing a value representing the folder's current view mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb5f2dd6-1257-4cfc-a222-88e6c3b524ce">GetDefaultSpacing</a>
</td>
<td align="left" width="63%">
Gets a pointer to a POINT structure containing the default width (x) and height (y) measurements of an item, including the surrounding white space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bbc0baf-b384-41da-850c-b2cb9570cb69">GetFocusedItem</a>
</td>
<td align="left" width="63%">
Gets the index of the item that currently has focus in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fdeb995-2220-4461-a4d6-80bce08153b1">GetFolder</a>
</td>
<td align="left" width="63%">
Gets the folder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/454d074c-1044-4626-8ec7-18e2adb4beca">GetItemPosition</a>
</td>
<td align="left" width="63%">
Gets the position of an item in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86416704-c2e3-4782-a566-b49cbd0e7696">GetSelectionMarkedItem</a>
</td>
<td align="left" width="63%">
Gets the index of an item in the folder's view which has been marked by using the SVSI_SELECTIONMARK in <a href="https://msdn.microsoft.com/6db262ea-861b-4bc5-955f-b81945313ea8">IFolderView::SelectItem</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea81c40-773f-4f53-97c1-99619e46be48">GetSpacing</a>
</td>
<td align="left" width="63%">
Gets a POINT structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c130ef36-1255-4c57-be31-7fc2029d9f66">Item</a>
</td>
<td align="left" width="63%">
Gets the identifier of a specific item in the folder view, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dadf91c5-7d27-4b1b-875b-6f0615440f47">ItemCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the folder. This can be the number of all items, or a subset such as the number of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f93e2d30-7b50-48e8-a3e7-6fa29abb8a32">Items</a>
</td>
<td align="left" width="63%">
Gets the address of an enumeration object based on the collection of items in the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1263bba8-63c8-4630-ab59-bb4ae10061fc">SelectAndPositionItems</a>
</td>
<td align="left" width="63%">
Allows the selection and positioning of items visible in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6db262ea-861b-4bc5-955f-b81945313ea8">SelectItem</a>
</td>
<td align="left" width="63%">
Selects an item in the folder's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ca42567-7bb9-41e1-8f2a-5f6d0309c636">SetCurrentViewMode</a>
</td>
<td align="left" width="63%">
Sets the selected folder's view mode.

</td>
</tr>
</table> 

