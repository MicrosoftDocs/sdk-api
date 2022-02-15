---
UID: NN:shobjidl_core.ICommDlgBrowser2
title: ICommDlgBrowser2 (shobjidl_core.h)
description: Extends the capabilities of ICommDlgBrowser. This interface is exposed by the common file dialog boxes when they host a Shell browser. A pointer to ICommDlgBrowser2 can be obtained by calling QueryInterface on the IShellBrowser object.
helpviewer_keywords: ["ICommDlgBrowser2","ICommDlgBrowser2 interface [Windows Shell]","ICommDlgBrowser2 interface [Windows Shell]","described","_win32_ICommDlgBrowser2","shell.ICommDlgBrowser2","shobjidl_core/ICommDlgBrowser2"]
old-location: shell\ICommDlgBrowser2.htm
tech.root: shell
ms.assetid: 07a416a2-340d-4308-a6f3-cf6f19f3c906
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser2, ICommDlgBrowser2 interface [Windows Shell], ICommDlgBrowser2 interface [Windows Shell],described, _win32_ICommDlgBrowser2, shell.ICommDlgBrowser2, shobjidl_core/ICommDlgBrowser2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICommDlgBrowser2
 - shobjidl_core/ICommDlgBrowser2
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
 - ICommDlgBrowser2
---

# ICommDlgBrowser2 interface


## -description

Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a>. This interface is exposed by the common file dialog boxes when they host a Shell browser. A pointer to <b>ICommDlgBrowser2</b> can be obtained by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> object.

## -inheritance

The <b>ICommDlgBrowser2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a>. <b>ICommDlgBrowser2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a> interface, from which it inherits.

<div class="alert"><b>Note</b>  In Windows XP and earlier, this interface was defined in Shlobj.h.</div>
<div> </div>
This interface is implemented only by common file dialog boxes.

Use <b>ICommDlgBrowser2</b> when your Shell view is hosted inside a common dialog box.

<b>ICommDlgBrowser2</b> implements all the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a> methods, as well as <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. The listed methods are specific to <b>ICommDlgBrowser2</b>.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
