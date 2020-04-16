---
UID: NN:shobjidl_core.ITaskbarList
title: ITaskbarList (shobjidl_core.h)
description: Exposes methods that control the taskbar. It allows you to dynamically add, remove, and activate items on the taskbar.helpviewer_keywords: ["ITaskbarList","ITaskbarList interface [Windows Shell]","ITaskbarList interface [Windows Shell]","described","_win32_ITaskbarList","shell.ITaskbarList","shobjidl_core/ITaskbarList"]
old-location: shell\ITaskbarList.htm
tech.root: shell
ms.assetid: c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38
ms.date: 12/05/2018
ms.keywords: ITaskbarList, ITaskbarList interface [Windows Shell], ITaskbarList interface [Windows Shell],described, _win32_ITaskbarList, shell.ITaskbarList, shobjidl_core/ITaskbarList
f1_keywords:
- shobjidl_core/ITaskbarList
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- ITaskbarList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskbarList interface


## -description


Exposes methods that control the taskbar. It allows you to dynamically add, remove, and activate items on the taskbar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskbarList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskbarList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskbarList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-activatetab">ActivateTab</a>
</td>
<td align="left" width="63%">
Activates an item on the taskbar. The window is not actually activated; the window's item on the taskbar is merely displayed as active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-addtab">AddTab</a>
</td>
<td align="left" width="63%">
Adds an item to the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-deletetab">DeleteTab</a>
</td>
<td align="left" width="63%">
Deletes an item from the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit">HrInit</a>
</td>
<td align="left" width="63%">
Initializes the taskbar list object. This method must be called before any other <b>ITaskbarList</b> methods can be called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-setactivealt">SetActiveAlt</a>
</td>
<td align="left" width="63%">
Marks a taskbar item as active but does not visually activate it.

</td>
</tr>
</table> 


## -remarks



You do not implement <b>ITaskbarList</b>; it is implemented by the Shell.

Use <b>ITaskbarList</b> to add items to the taskbar, remove items from the taskbar, and activate items on the taskbar.

See <a href="https://docs.microsoft.com/windows/desktop/shell/taskbar">Modifying Contents of the Taskbar</a> for more information about using this interface.



