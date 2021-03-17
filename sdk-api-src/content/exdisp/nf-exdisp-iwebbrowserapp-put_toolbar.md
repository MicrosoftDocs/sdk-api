---
UID: NF:exdisp.IWebBrowserApp.put_ToolBar
title: IWebBrowserApp::put_ToolBar (exdisp.h)
description: Sets or gets whether toolbars for the object are visible.
helpviewer_keywords: ["FALSE","IWebBrowser2 interface [Windows API]","ToolBar property","IWebBrowser2.ToolBar","IWebBrowser2.get_ToolBar","IWebBrowser2.put_ToolBar","IWebBrowser2::get_ToolBar","IWebBrowser2::put_ToolBar","IWebBrowserApp interface [Windows API]","ToolBar property","IWebBrowserApp.ToolBar","IWebBrowserApp.put_ToolBar","IWebBrowserApp::ToolBar","IWebBrowserApp::get_ToolBar","IWebBrowserApp::put_ToolBar","TRUE","ToolBar property [Windows API]","ToolBar property [Windows API]","IWebBrowser2 interface","ToolBar property [Windows API]","IWebBrowserApp interface","exdisp/IWebBrowser2::ToolBar","exdisp/IWebBrowser2::get_ToolBar","exdisp/IWebBrowser2::put_ToolBar","exdisp/IWebBrowserApp::ToolBar","exdisp/IWebBrowserApp::get_ToolBar","exdisp/IWebBrowserApp::put_ToolBar","put_ToolBar","winprog.iwebbrowser2_toolbar"]
old-location: winprog\iwebbrowser2_toolbar.htm
tech.root: winprog
ms.assetid: 25C459AF-A57C-453A-987C-004CCA8F276F
ms.date: 12/05/2018
ms.keywords: FALSE, IWebBrowser2 interface [Windows API],ToolBar property, IWebBrowser2.ToolBar, IWebBrowser2.get_ToolBar, IWebBrowser2.put_ToolBar, IWebBrowser2::get_ToolBar, IWebBrowser2::put_ToolBar, IWebBrowserApp interface [Windows API],ToolBar property, IWebBrowserApp.ToolBar, IWebBrowserApp.put_ToolBar, IWebBrowserApp::ToolBar, IWebBrowserApp::get_ToolBar, IWebBrowserApp::put_ToolBar, TRUE, ToolBar property [Windows API], ToolBar property [Windows API],IWebBrowser2 interface, ToolBar property [Windows API],IWebBrowserApp interface, exdisp/IWebBrowser2::ToolBar, exdisp/IWebBrowser2::get_ToolBar, exdisp/IWebBrowser2::put_ToolBar, exdisp/IWebBrowserApp::ToolBar, exdisp/IWebBrowserApp::get_ToolBar, exdisp/IWebBrowserApp::put_ToolBar, put_ToolBar, winprog.iwebbrowser2_toolbar
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Shdocvw.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWebBrowserApp::put_ToolBar
 - exdisp/IWebBrowserApp::put_ToolBar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
 - Shdocvw.dll.dll
api_name:
 - IWebBrowserApp.ToolBar
 - IWebBrowserApp.get_ToolBar
 - IWebBrowserApp.put_ToolBar
 - IWebBrowser2.ToolBar
 - IWebBrowser2.get_ToolBar
 - IWebBrowser2.put_ToolBar
 - IWebBrowser2.get_ToolBar
 - IWebBrowser2.put_ToolBar
---

# IWebBrowserApp::put_ToolBar


## -description

Sets or gets whether toolbars for the object are visible.

This property is read/write.

## -parameters

## -remarks

When the IWebBrowser2::ToolBar property is set to FALSE, it is not equivalent to the "toolbar=no" feature of window.open. Instead, it turns off all user interface elements that can be considered toolbars, leaving Windows Internet Explorer in a blank state. 

The WebBrowser object saves the value of this property, but otherwise ignores it.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-iwebbrowser2">IWebBrowser2</a>