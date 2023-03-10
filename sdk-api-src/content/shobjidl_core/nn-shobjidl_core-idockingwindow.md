---
UID: NN:shobjidl_core.IDockingWindow
title: IDockingWindow (shobjidl_core.h)
description: Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal. This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.
helpviewer_keywords: ["IDockingWindow","IDockingWindow interface [Windows Shell]","IDockingWindow interface [Windows Shell]","described","_win32_IDockingWindow","shell.IDockingWindow","shobjidl_core/IDockingWindow"]
old-location: shell\IDockingWindow.htm
tech.root: shell
ms.assetid: 9e80fd5e-f57d-4801-b198-73b8f5ffff6e
ms.date: 12/05/2018
ms.keywords: IDockingWindow, IDockingWindow interface [Windows Shell], IDockingWindow interface [Windows Shell],described, _win32_IDockingWindow, shell.IDockingWindow, shobjidl_core/IDockingWindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDockingWindow
 - shobjidl_core/IDockingWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDockingWindow
---

# IDockingWindow interface


## -description

Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal. This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.

## -inheritance

The <b>IDockingWindow</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IDockingWindow</b> also has these types of members:

## -remarks

<b>IDockingWindow</b> is derived from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindow</b> through that inheritance.



<table class="clsStd">
<tr>
<th>Additional IDockingWindow Methods</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">IDockingWindow::GetWindow</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp">IDockingWindow::ContextSensitiveHelp</a>
</td>
</tr>
</table>
 

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IDockingWindow</b> when you want to display a window inside a browser frame. This is typically used for user interface windows, such as toolbars.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not usually use the <b>IDockingWindow</b> interface directly. The Shell browser uses this interface to support docked windows inside the browser frame.
