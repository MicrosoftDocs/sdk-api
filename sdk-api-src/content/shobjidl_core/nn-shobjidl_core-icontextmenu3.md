---
UID: NN:shobjidl_core.IContextMenu3
title: IContextMenu3
author: windows-sdk-content
description: Exposes methods that either create or merge a shortcut menu associated with a Shell object. Allows client objects to handle messages associated with owner-drawn menu items and extends IContextMenu2 by accepting a return value from that message handling.
old-location: shell\IContextMenu3.htm
tech.root: shell
ms.assetid: c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IContextMenu3, IContextMenu3 interface [Windows Shell], IContextMenu3 interface [Windows Shell],described, _win32_IContextMenu3, shell.IContextMenu3, shobjidl_core/IContextMenu3
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
req.idl: Shobjidl.idl
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
 - IContextMenu3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextMenu3 interface


## -description


Exposes methods that either create or merge a shortcut menu associated with a Shell object. Allows client objects to handle messages associated with owner-drawn menu items and extends <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a> by accepting a return value from that message handling.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenu3</b> interface inherits from <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a>. <b>IContextMenu3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenu3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d258edb1-9489-4cdf-b398-16af37a1cb38">HandleMenuMsg2</a>
</td>
<td align="left" width="63%">
Allows client objects of the <b>IContextMenu3</b> interface to handle messages associated with owner-drawn menu items.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> and <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IContextMenu3</b> if your shortcut menu extension needs to process the <a href="https://msdn.microsoft.com/de6c91bb-80fd-44b2-8d96-d016477a6547">WM_MENUCHAR</a> message.

			    

This message is forwarded to <a href="https://msdn.microsoft.com/d258edb1-9489-4cdf-b398-16af37a1cb38">IContextMenu3::HandleMenuMsg2</a> only if a <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call for an <b>IContextMenu3</b> interface pointer is successful, which indicates that the object supports this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not call this interface directly. <b>IContextMenu3</b> is used by the operating system only when it has confirmed that your application is aware of this interface.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


