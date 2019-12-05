---
UID: NN:shobjidl_core.ICommDlgBrowser
title: ICommDlgBrowser (shobjidl_core.h)
description: Exposed by the common file dialog boxes to be used when they host a Shell browser.
old-location: shell\ICommDlgBrowser.htm
tech.root: shell
ms.assetid: bf89ac6e-6c2e-4944-885c-9ab62f58fe71
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser, ICommDlgBrowser interface [Windows Shell], ICommDlgBrowser interface [Windows Shell],described, _win32_ICommDlgBrowser, shell.ICommDlgBrowser, shobjidl_core/ICommDlgBrowser
ms.topic: interface
f1_keywords:
- shobjidl_core/ICommDlgBrowser
dev_langs:
- c++
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
- ICommDlgBrowser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICommDlgBrowser interface


## -description


Exposed by the common file dialog boxes to be used when they host a Shell browser. If supported, <b>ICommDlgBrowser</b> exposes methods that allow a Shell view to handle several cases that require different behavior in a dialog box than in a normal Shell view. You obtain an <b>ICommDlgBrowser</b> interface pointer by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommDlgBrowser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICommDlgBrowser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommDlgBrowser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser-includeobject">IncludeObject</a>
</td>
<td align="left" width="63%">
Allows the common dialog box to filter objects that the view displays.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser-ondefaultcommand">OnDefaultCommand</a>
</td>
<td align="left" width="63%">
Called when a user double-clicks in the view or presses the ENTER key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser-onstatechange">OnStateChange</a>
</td>
<td align="left" width="63%">
Called after a state, identified by the <i>uChange</i> parameter, has changed in the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  In Windows XP and earlier, this interface was defined in Shlobj.h.
      </div>
<div> </div>
This interface is implemented only by the common file dialog boxes.

Use <b>ICommDlgBrowser</b> when you need to provide special behavior while hosted inside the common dialog boxes.
      



