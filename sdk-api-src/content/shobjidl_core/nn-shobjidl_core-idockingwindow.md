---
UID: NN:shobjidl_core.IDockingWindow
title: IDockingWindow (shobjidl_core.h)

description: Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal. This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.
old-location: shell\IDockingWindow.htm
tech.root: shell
ms.assetid: 9e80fd5e-f57d-4801-b198-73b8f5ffff6e

ms.date: 12/05/2018
ms.keywords: IDockingWindow, IDockingWindow interface [Windows Shell], IDockingWindow interface [Windows Shell],described, _win32_IDockingWindow, shell.IDockingWindow, shobjidl_core/IDockingWindow
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IDockingWindow"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDockingWindow interface


## -description


Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal. This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDockingWindow</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IDockingWindow</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw">CloseDW</a>
</td>
<td align="left" width="63%">
Notifies the docking window object that it is about to be removed from the frame. The docking window object should save any persistent information at this time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw">ResizeBorderDW</a>
</td>
<td align="left" width="63%">
Notifies the docking window object that the frame's border space has changed. In response to this method, the <b>IDockingWindow</b> implementation must call <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-setborderspacedw">IDockingWindowSite::SetBorderSpaceDW</a>, even if no border space is required or a change is not necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw">ShowDW</a>
</td>
<td align="left" width="63%">
Instructs the docking window object to show or hide itself.

</td>
</tr>
</table> 


## -remarks



<b>IDockingWindow</b> is derived from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindow</b> through that inheritance.



<table class="clsStd">
<tr>
<th>Additional IDockingWindow Methods</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">IDockingWindow::GetWindow</a>
</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp">IDockingWindow::ContextSensitiveHelp</a>
</td>
</tr>
</table>
 

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IDockingWindow</b> when you want to display a window inside a browser frame. This is typically used for user interface windows, such as toolbars.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not usually use the <b>IDockingWindow</b> interface directly. The Shell browser uses this interface to support docked windows inside the browser frame.



