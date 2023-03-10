---
UID: NN:shobjidl_core.IShellBrowser
title: IShellBrowser (shobjidl_core.h)
description: Implemented by hosts of Shell views (objects that implement IShellView). Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window.
helpviewer_keywords: ["IShellBrowser","IShellBrowser interface [Windows Shell]","IShellBrowser interface [Windows Shell]","described","_win32_IShellBrowser","shell.IShellBrowser","shobjidl_core/IShellBrowser"]
old-location: shell\IShellBrowser.htm
tech.root: shell
ms.assetid: 138d90e3-a1f0-4faf-88ca-16c7a46df0ca
ms.date: 12/05/2018
ms.keywords: IShellBrowser, IShellBrowser interface [Windows Shell], IShellBrowser interface [Windows Shell],described, _win32_IShellBrowser, shell.IShellBrowser, shobjidl_core/IShellBrowser
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - IShellBrowser
 - shobjidl_core/IShellBrowser
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
 - IShellBrowser
---

# IShellBrowser interface


## -description

Implemented by hosts of Shell views (objects that implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>). Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window.

## -inheritance

The <b>IShellBrowser</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IShellBrowser</b> also has these types of members:

## -remarks

Windows Explorer and the <b>Open File</b> common dialog box are examples of implementations of this interface. It is a companion to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface exposed by extensions.



Objects that have access to the site chain of the browser can get a reference to the browser on <b>IShellBrowser</b> using  <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a>, with Service IDs such as SID_STopLevelBrowser and SID_SCommDlgBrowser.

<b>Windows 7 and later</b>.  Windows Explorer context menus  can support in-place navigation by using  <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a> with the Service ID SID_SlnPlaceBrowser.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
