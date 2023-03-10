---
UID: NN:shobjidl_core.ICommDlgBrowser
title: ICommDlgBrowser (shobjidl_core.h)
description: Exposed by the common file dialog boxes to be used when they host a Shell browser.
helpviewer_keywords: ["ICommDlgBrowser","ICommDlgBrowser interface [Windows Shell]","ICommDlgBrowser interface [Windows Shell]","described","_win32_ICommDlgBrowser","shell.ICommDlgBrowser","shobjidl_core/ICommDlgBrowser"]
old-location: shell\ICommDlgBrowser.htm
tech.root: shell
ms.assetid: bf89ac6e-6c2e-4944-885c-9ab62f58fe71
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser, ICommDlgBrowser interface [Windows Shell], ICommDlgBrowser interface [Windows Shell],described, _win32_ICommDlgBrowser, shell.ICommDlgBrowser, shobjidl_core/ICommDlgBrowser
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICommDlgBrowser
 - shobjidl_core/ICommDlgBrowser
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
 - ICommDlgBrowser
---

# ICommDlgBrowser interface


## -description

Exposed by the common file dialog boxes to be used when they host a Shell browser. If supported, <b>ICommDlgBrowser</b> exposes methods that allow a Shell view to handle several cases that require different behavior in a dialog box than in a normal Shell view. You obtain an <b>ICommDlgBrowser</b> interface pointer by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> object.

## -inheritance

The <b>ICommDlgBrowser</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICommDlgBrowser</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  In Windows XP and earlier, this interface was defined in Shlobj.h.
      </div>
<div> </div>
This interface is implemented only by the common file dialog boxes.

Use <b>ICommDlgBrowser</b> when you need to provide special behavior while hosted inside the common dialog boxes.
