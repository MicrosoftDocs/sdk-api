---
UID: NF:exdisp.IWebBrowserApp.get_ToolBar
title: IWebBrowserApp::get_ToolBar
author: windows-sdk-content
description: Sets or gets whether toolbars for the object are visible.
old-location: winprog\iwebbrowser2_toolbar.htm
tech.root: DevNotes
ms.assetid: 25C459AF-A57C-453A-987C-004CCA8F276F
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FALSE, IWebBrowser2 interface [Windows API],ToolBar property, IWebBrowser2.ToolBar, IWebBrowser2.get_ToolBar, IWebBrowser2.put_ToolBar, IWebBrowser2::get_ToolBar, IWebBrowser2::put_ToolBar, IWebBrowserApp interface [Windows API],ToolBar property, IWebBrowserApp.ToolBar, IWebBrowserApp.get_ToolBar, IWebBrowserApp::ToolBar, IWebBrowserApp::get_ToolBar, IWebBrowserApp::put_ToolBar, TRUE, ToolBar property [Windows API], ToolBar property [Windows API],IWebBrowser2 interface, ToolBar property [Windows API],IWebBrowserApp interface, exdisp/IWebBrowser2::ToolBar, exdisp/IWebBrowser2::get_ToolBar, exdisp/IWebBrowser2::put_ToolBar, exdisp/IWebBrowserApp::ToolBar, exdisp/IWebBrowserApp::get_ToolBar, exdisp/IWebBrowserApp::put_ToolBar, get_ToolBar, winprog.iwebbrowser2_toolbar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebBrowserApp::get_ToolBar


## -description


Sets or gets whether toolbars for the object are visible.

This property is read/write.


## -parameters


## -remarks



When the IWebBrowser2::ToolBar property is set to FALSE, it is not equivalent to the "toolbar=no" feature of window.open. Instead, it turns off all user interface elements that can be considered toolbars, leaving Windows Internet Explorer in a blank state. 

The WebBrowser object saves the value of this property, but otherwise ignores it. 




## -see-also




<a href="https://msdn.microsoft.com/AFED694C-8D7B-4539-9A1A-B2DA546F3A07">IWebBrowser2</a>
 

 

