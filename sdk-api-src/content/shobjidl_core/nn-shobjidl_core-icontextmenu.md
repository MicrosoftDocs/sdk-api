---
UID: NN:shobjidl_core.IContextMenu
title: IContextMenu
author: windows-sdk-content
description: Exposes methods that either create or merge a shortcut menu associated with a Shell object.
old-location: shell\IContextMenu.htm
tech.root: shell
ms.assetid: 6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IContextMenu, IContextMenu interface [Windows Shell], IContextMenu interface [Windows Shell],described, _win32_IContextMenu, _win32_icontextmenu_cpp, shell.IContextMenu, shobjidl_core/IContextMenu
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
 - IContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextMenu interface


## -description


Exposes methods that either create or merge a shortcut menu associated with a Shell object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenu</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContextMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efa60153-7635-4aef-bd9e-f51fe4ecc234">GetCommandString</a>
</td>
<td align="left" width="63%">
Gets information about a shortcut menu command, including the help string and the language-independent, or <i>canonical</i>, name for the command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">InvokeCommand</a>
</td>
<td align="left" width="63%">
Carries out the command associated with a shortcut menu item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/329fe15b-c1c1-4ffd-812e-9e74451bad6e">QueryContextMenu</a>
</td>
<td align="left" width="63%">
Adds commands to a shortcut menu.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IContextMenu</b> in the following situations.
				

<ul>
<li>
<a href="https://msdn.microsoft.com/74a81e4f-7357-4901-a118-ba44e8892f25">Shell extension handlers</a> implement this interface to dynamically add items to a Shell object's shortcut menu.</li>
<li>
<a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">Namespace extensions</a> implement this interface to specify their object's shortcut menus.</li>
</ul>
For a detailed discussion of how to implement <b>IContextMenu</b>, see <a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">Creating Context Menu Handlers</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications use <b>IContextMenu</b> to retrieve information about the items in an object's shortcut menu and to invoke the associated commands. To retrieve an object's <b>IContextMenu</b> interface, an application must call the object's <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> method.

Shell extension handlers that export this interface must also export <a href="https://msdn.microsoft.com/5f7e7f71-4cd6-4ce4-946c-9a1f7ec72fbe">IShellExtInit</a>. For details, see <a href="https://msdn.microsoft.com/74a81e4f-7357-4901-a118-ba44e8892f25">Creating Shell Extension Handlers</a>.

<div class="alert"><b>Note</b>  <b>Windows Vista and later:</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


