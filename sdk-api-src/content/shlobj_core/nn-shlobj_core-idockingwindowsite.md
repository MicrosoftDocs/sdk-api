---
UID: NN:shlobj_core.IDockingWindowSite
title: IDockingWindowSite (shlobj_core.h)
description: Exposes methods that manage the border space for one or more IDockingWindow objects. This interface is implemented by the browser and is similar to the IOleInPlaceUIWindow interface.
helpviewer_keywords: ["IDockingWindowSite","IDockingWindowSite interface [Windows Shell]","IDockingWindowSite interface [Windows Shell]","described","_win32_IDockingWindowSite","shell.IDockingWindowSite","shlobj_core/IDockingWindowSite"]
old-location: shell\IDockingWindowSite.htm
tech.root: shell
ms.assetid: 7418a6af-74ce-4435-8ed9-af106df0f95b
ms.date: 12/05/2018
ms.keywords: IDockingWindowSite, IDockingWindowSite interface [Windows Shell], IDockingWindowSite interface [Windows Shell],described, _win32_IDockingWindowSite, shell.IDockingWindowSite, shlobj_core/IDockingWindowSite
req.header: shlobj_core.h
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
 - IDockingWindowSite
 - shlobj_core/IDockingWindowSite
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
 - IDockingWindowSite
---

# IDockingWindowSite interface


## -description

Exposes methods that manage the border space for one or more <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> objects. This interface is implemented by the browser and is similar to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a> interface.

## -inheritance

The <b>IDockingWindowSite</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IDockingWindowSite</b> also has these types of members:

## -remarks

<b>IDockingWindowSite</b> is derived from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindowSite</b> through that inheritance.



<table class="clsStd">
<tr>
<th>Additional IDockingWindowSite Methods</th>
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
You do not typically implement the <b>IDockingWindowSite</b> interface. The Shell browser implements this interface to support docked windows inside the browser frame.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You use <b>IDockingWindowSite</b> to negotiate the space for a docking window object in a browser frame.
