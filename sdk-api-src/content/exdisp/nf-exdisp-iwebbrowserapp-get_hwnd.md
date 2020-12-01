---
UID: NF:exdisp.IWebBrowserApp.get_HWND
title: IWebBrowserApp::get_HWND (exdisp.h)
description: Gets the handle of the Windows Internet Explorer main window.
helpviewer_keywords: ["HWND property [Windows API]","HWND property [Windows API]","IWebBrowser2 interface","HWND property [Windows API]","IWebBrowserApp interface","IWebBrowser2 interface [Windows API]","HWND property","IWebBrowser2.HWND","IWebBrowser2.get_HWND","IWebBrowser2::get_HWND","IWebBrowserApp interface [Windows API]","HWND property","IWebBrowserApp.HWND","IWebBrowserApp.get_HWND","IWebBrowserApp::HWND","IWebBrowserApp::get_HWND","exdisp/IWebBrowser2::HWND","exdisp/IWebBrowser2::get_HWND","exdisp/IWebBrowserApp::HWND","exdisp/IWebBrowserApp::get_HWND","get_HWND","nHWND","winprog.iwebbrowser2_hwnd"]
old-location: winprog\iwebbrowser2_hwnd.htm
tech.root: winprog
ms.assetid: 4A37C795-C8C7-4861-A03D-E56D9BD8FF5D
ms.date: 12/05/2018
ms.keywords: HWND property [Windows API], HWND property [Windows API],IWebBrowser2 interface, HWND property [Windows API],IWebBrowserApp interface, IWebBrowser2 interface [Windows API],HWND property, IWebBrowser2.HWND, IWebBrowser2.get_HWND, IWebBrowser2::get_HWND, IWebBrowserApp interface [Windows API],HWND property, IWebBrowserApp.HWND, IWebBrowserApp.get_HWND, IWebBrowserApp::HWND, IWebBrowserApp::get_HWND, exdisp/IWebBrowser2::HWND, exdisp/IWebBrowser2::get_HWND, exdisp/IWebBrowserApp::HWND, exdisp/IWebBrowserApp::get_HWND, get_HWND, nHWND, winprog.iwebbrowser2_hwnd
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
 - IWebBrowserApp::get_HWND
 - exdisp/IWebBrowserApp::get_HWND
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
 - IWebBrowserApp.HWND
 - IWebBrowserApp.get_HWND
 - IWebBrowser2.HWND
 - IWebBrowser2.get_HWND
 - IWebBrowser2.get_HWND
---

# IWebBrowserApp::get_HWND


## -description

Gets the handle of the Windows Internet Explorer main window.

This property is read-only.

## -parameters

## -remarks

Internet Explorer 7. With the introduction of tabbed browsing, the return value of this method can be ambiguous. To alleviate confusion and maintain the highest level of compatibility with existing applications, this method returns a handle to the top-level window frame, not the currently selected tab.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-iwebbrowser2">IWebBrowser2</a>