---
UID: NN:shlobj.IDockingWindowFrame
title: IDockingWindowFrame (shlobj.h)
description: Exposes methods that support the addition of IDockingWindow objects to a frame. Implemented by the browser.
helpviewer_keywords: ["IDockingWindowFrame","IDockingWindowFrame interface [Windows Shell]","IDockingWindowFrame interface [Windows Shell]","described","_win32_IDockingWindowFrame","shell.IDockingWindowFrame","shlobj/IDockingWindowFrame"]
old-location: shell\IDockingWindowFrame.htm
tech.root: shell
ms.assetid: d0dc10db-316a-4eaa-83db-3f186ee77071
ms.date: 12/05/2018
ms.keywords: IDockingWindowFrame, IDockingWindowFrame interface [Windows Shell], IDockingWindowFrame interface [Windows Shell],described, _win32_IDockingWindowFrame, shell.IDockingWindowFrame, shlobj/IDockingWindowFrame
req.header: shlobj.h
req.include-header: 
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
 - IDockingWindowFrame
 - shlobj/IDockingWindowFrame
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
 - IDockingWindowFrame
---

# IDockingWindowFrame interface


## -description

Exposes methods that support the addition of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> objects to a frame. Implemented by the browser.

## -inheritance

The <b>IDockingWindowFrame</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IDockingWindowFrame</b> also has these types of members:

## -remarks

<b>IDockingWindowFrame</b> is derived from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindowFrame</b> through that inheritance.

<table class="clsStd">
<tr>
<th>Additional IDockingWindowFrame Methods</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">IOleWindow::GetWindow</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp">IOleWindow::ContextSensitiveHelp</a>
</td>
</tr>
</table>
 

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You do not typically implement the <b>IDockingWindowFrame</b> interface. The Shell browser implements this interface to support docked windows inside the browser frame.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You use <b>IDockingWindowFrame</b> to add, find, and remove docking window objects in a browser frame.
