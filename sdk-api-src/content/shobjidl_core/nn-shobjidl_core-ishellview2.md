---
UID: NN:shobjidl_core.IShellView2
title: IShellView2
author: windows-sdk-content
description: Extends the capabilities of IShellView.
old-location: shell\IShellView2.htm
tech.root: shell
ms.assetid: a61aec39-406d-4066-941d-e788d64f4310
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IShellView2, IShellView2 interface [Windows Shell], IShellView2 interface [Windows Shell],described, _win32_IShellView2, shell.IShellView2, shobjidl_core/IShellView2
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
 - IShellView2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView2 interface


## -description


Extends the capabilities of <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellView2</b> interface inherits from <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>. <b>IShellView2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellView2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b829f5f-26ea-4987-be05-6725eeff5fed">CreateViewWindow2</a>
</td>
<td align="left" width="63%">
Used to request the creation of a new Shell view window. It can be either the right pane of Windows Explorer or the client window of a folder window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74fe42fe-33de-483a-88e4-50da9c1f77c2">GetView</a>
</td>
<td align="left" width="63%">
Requests the current or default Shell view, together with all other valid view identifiers (VIDs) supported by this implementation of <b>IShellView2</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0264df56-433f-4c54-a7e0-ccd92d3da602">HandleRename</a>
</td>
<td align="left" width="63%">
Used to change an item's identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d78f152b-2dcb-410d-821a-56601a3c57f2">SelectAndPositionItem</a>
</td>
<td align="left" width="63%">
Selects and positions an item in a Shell View.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IShellView2</b> if your namespace extension provides services to clients beyond those in <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not call this interface directly. <b>IShellView2</b> is used by the operating system only when it has confirmed that your application is aware of this interface. Objects that expose <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> and <b>IShellView2</b> are usually created by other Shell folder objects.



