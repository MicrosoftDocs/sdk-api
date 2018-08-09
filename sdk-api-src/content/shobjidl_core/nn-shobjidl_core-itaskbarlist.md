---
UID: NN:shobjidl_core.ITaskbarList
title: ITaskbarList
author: windows-sdk-content
description: Exposes methods that control the taskbar. It allows you to dynamically add, remove, and activate items on the taskbar.
old-location: shell\ITaskbarList.htm
old-project: shell
ms.assetid: c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITaskbarList, ITaskbarList interface [Windows Shell], ITaskbarList interface [Windows Shell],described, _win32_ITaskbarList, shell.ITaskbarList, shobjidl_core/ITaskbarList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ITaskbarList
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ITaskbarList interface


## -description


Exposes methods that control the taskbar. It allows you to dynamically add, remove, and activate items on the taskbar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskbarList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskbarList</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1dc95768-62a5-4784-9f4f-96bebdd38c2b">ActivateTab</a>
</td>
<td align="left" width="63%">
Activates an item on the taskbar. The window is not actually activated; the window's item on the taskbar is merely displayed as active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47d52ab8-f182-4bfb-8745-ad2d23197088">AddTab</a>
</td>
<td align="left" width="63%">
Adds an item to the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf1b3d27-5cd3-44c8-81e6-d9418d30ffe3">DeleteTab</a>
</td>
<td align="left" width="63%">
Deletes an item from the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0344bf0b-b460-4516-88eb-09131cc9a4f8">HrInit</a>
</td>
<td align="left" width="63%">
Initializes the taskbar list object. This method must be called before any other <b>ITaskbarList</b> methods can be called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9d08a72-6a4d-483b-bf12-3f78e1d2237a">SetActiveAlt</a>
</td>
<td align="left" width="63%">
Marks a taskbar item as active but does not visually activate it.

</td>
</tr>
</table> 


## -remarks



You do not implement <b>ITaskbarList</b>; it is implemented by the Shell.

Use <b>ITaskbarList</b> to add items to the taskbar, remove items from the taskbar, and activate items on the taskbar.

See <a href="https://msdn.microsoft.com/14d520e7-7c15-441d-9662-24b972d208ac">Modifying Contents of the Taskbar</a> for more information about using this interface.



