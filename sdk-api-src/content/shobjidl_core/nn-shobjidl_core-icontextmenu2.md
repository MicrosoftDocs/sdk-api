---
UID: NN:shobjidl_core.IContextMenu2
title: IContextMenu2
author: windows-sdk-content
description: Exposes methods that either create or merge a shortcut (context) menu associated with a Shell object. Extends IContextMenu by adding a method that allows client objects to handle messages associated with owner-drawn menu items.
old-location: shell\IContextMenu2.htm
tech.root: shell
ms.assetid: 4e3331ad-4adc-4ea9-8a22-6aad15f618c8
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IContextMenu2, IContextMenu2 interface [Windows Shell], IContextMenu2 interface [Windows Shell],described, _win32_IContextMenu2, shell.IContextMenu2, shobjidl_core/IContextMenu2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IContextMenu2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextMenu2 interface


## -description


Exposes methods that either create or merge a shortcut (context) menu associated with a Shell object. Extends <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> by adding a method that allows client objects to handle messages associated with owner-drawn menu items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenu2</b> interface inherits from <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>. <b>IContextMenu2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenu2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06ea4563-a299-4587-906f-4f312c21498a">HandleMenuMsg</a>
</td>
<td align="left" width="63%">
Enables client objects of the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> interface to handle messages associated with owner-drawn menu items.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> interface, from which it inherits.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IContextMenu2</b> if your <a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">namespace extension</a> or <a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">shortcut menu handler</a> needs to process one or more of the following messages. 

				

<ul>
<li>
<a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e54bae5e-10d6-43b0-a766-1b270c8873a9">WM_DRAWITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6947bcd1-fd40-4238-b8f2-d4e06b90c0dc">WM_MEASUREITEM</a>
</li>
</ul>
These messages are forwarded to <b>IContextMenu2</b>—through the <a href="https://msdn.microsoft.com/06ea4563-a299-4587-906f-4f312c21498a">HandleMenuMsg</a> method—only if a <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call for an <b>IContextMenu2</b> interface pointer is successful, indicating that the object supports this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications do not normally call this interface directly.



