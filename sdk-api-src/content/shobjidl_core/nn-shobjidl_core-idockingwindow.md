---
UID: NN:shobjidl_core.IDockingWindow
title: IDockingWindow (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal. This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.
old-location: shell\IDockingWindow.htm
tech.root: shell
ms.assetid: 9e80fd5e-f57d-4801-b198-73b8f5ffff6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDockingWindow, IDockingWindow interface [Windows Shell], IDockingWindow interface [Windows Shell],described, _win32_IDockingWindow, shell.IDockingWindow, shobjidl_core/IDockingWindow
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shlobj.h
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
 - IDockingWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindow interface


## -description


Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal. This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDockingWindow</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IDockingWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDockingWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29e57436-cc8f-46e8-bc1a-b44bd803c4a8">CloseDW</a>
</td>
<td align="left" width="63%">
Notifies the docking window object that it is about to be removed from the frame. The docking window object should save any persistent information at this time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de61badd-0794-484c-921f-4e72e881579c">ResizeBorderDW</a>
</td>
<td align="left" width="63%">
Notifies the docking window object that the frame's border space has changed. In response to this method, the <b>IDockingWindow</b> implementation must call <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">IDockingWindowSite::SetBorderSpaceDW</a>, even if no border space is required or a change is not necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c33031d4-f9f4-4210-93be-963e5f299408">ShowDW</a>
</td>
<td align="left" width="63%">
Instructs the docking window object to show or hide itself.

</td>
</tr>
</table> 


## -remarks



<b>IDockingWindow</b> is derived from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindow</b> through that inheritance.



<table class="clsStd">
<tr>
<th>Additional IDockingWindow Methods</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">IDockingWindow::GetWindow</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/253f26c6-b5dd-4837-9135-96e11b4688c8">IDockingWindow::ContextSensitiveHelp</a>
</td>
</tr>
</table>
 

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IDockingWindow</b> when you want to display a window inside a browser frame. This is typically used for user interface windows, such as toolbars.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not usually use the <b>IDockingWindow</b> interface directly. The Shell browser uses this interface to support docked windows inside the browser frame.



