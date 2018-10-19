---
UID: NN:shobjidl_core.IShellExtInit
title: IShellExtInit
author: windows-sdk-content
description: Exposes a method that initializes Shell extensions for property sheets, shortcut menus, and drag-and-drop handlers (extensions that add items to shortcut menus during nondefault drag-and-drop operations).
old-location: shell\IShellExtInit.htm
tech.root: shell
ms.assetid: 5f7e7f71-4cd6-4ce4-946c-9a1f7ec72fbe
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IShellExtInit, IShellExtInit interface [Windows Shell], IShellExtInit interface [Windows Shell],described, _win32_IShellExtInit, _win32_ishellextinit_cpp, shell.IShellExtInit, shobjidl_core/IShellExtInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellExtInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellExtInit interface


## -description


Exposes a method that initializes Shell extensions for property sheets, shortcut menus, and drag-and-drop handlers (extensions that add items to shortcut menus during nondefault drag-and-drop operations).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellExtInit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellExtInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellExtInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1997a32e-562a-4d20-ad09-c40446a8feed">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a property sheet extension, shortcut menu extension, or drag-and-drop handler.

</td>
</tr>
</table> 


## -remarks



Implement <b>IShellExtInit</b> when you are writing a handler based on the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> or <a href="https://msdn.microsoft.com/1671ad3e-c131-4de0-a213-b22c9966bae2">IShellPropSheetExt</a> interface.

Note that Shell extensions based on other interfaces do not use this method of initialization.

You do not use this interface directly. The Shell calls it to initialize the handler.



