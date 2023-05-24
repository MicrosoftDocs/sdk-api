---
UID: NF:exdisp.IWebBrowser2.put_TheaterMode
title: IWebBrowser2::put_TheaterMode (exdisp.h)
description: Sets or gets whether the object is in theater mode. (Put)
helpviewer_keywords: ["IWebBrowser2 interface [Windows API]","TheaterMode property","IWebBrowser2.TheaterMode","IWebBrowser2.get_TheaterMode","IWebBrowser2.put_TheaterMode","IWebBrowser2::TheaterMode","IWebBrowser2::get_TheaterMode","IWebBrowser2::put_TheaterMode","TheaterMode property [Windows API]","TheaterMode property [Windows API]","IWebBrowser2 interface","VARIANT_FALSE","VARIANT_TRUE","exdisp/IWebBrowser2::TheaterMode","exdisp/IWebBrowser2::get_TheaterMode","exdisp/IWebBrowser2::put_TheaterMode","put_TheaterMode","winprog.iwebbrowser2_theatermode"]
old-location: winprog\iwebbrowser2_theatermode.htm
tech.root: winprog
ms.assetid: 78E8B986-ABA2-47A3-AED2-97A84C10C80A
ms.date: 12/05/2018
ms.keywords: IWebBrowser2 interface [Windows API],TheaterMode property, IWebBrowser2.TheaterMode, IWebBrowser2.get_TheaterMode, IWebBrowser2.put_TheaterMode, IWebBrowser2::TheaterMode, IWebBrowser2::get_TheaterMode, IWebBrowser2::put_TheaterMode, TheaterMode property [Windows API], TheaterMode property [Windows API],IWebBrowser2 interface, VARIANT_FALSE, VARIANT_TRUE, exdisp/IWebBrowser2::TheaterMode, exdisp/IWebBrowser2::get_TheaterMode, exdisp/IWebBrowser2::put_TheaterMode, put_TheaterMode, winprog.iwebbrowser2_theatermode
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
 - IWebBrowser2::put_TheaterMode
 - exdisp/IWebBrowser2::put_TheaterMode
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
 - IWebBrowser2.TheaterMode
 - IWebBrowser2.get_TheaterMode
 - IWebBrowser2.put_TheaterMode
 - IWebBrowser2.put_TheaterMode
 - IWebBrowser2.get_TheaterMode
---

# IWebBrowser2::put_TheaterMode


## -description

Sets or gets whether the object is in theater mode.

This property is read/write.

## -parameters

## -remarks

In theater mode, the object's main window fills the entire screen and displays a toolbar that has a minimal set of navigational buttons. A status bar is also provided in the upper-right corner of the screen. Explorer bars, such as  History  and Favorites , are displayed as an autohide pane on the left edge of the screen in theater mode. 

Setting TheaterMode (even to VARIANT_FALSE) resets the values of the IWebBrowser2::AddressBar and IWebBrowser2::ToolBar properties to VARIANT_TRUE. Disable the address bar and toolbars after you set the TheaterMode property. 

The WebBrowser object saves the value of this property, but otherwise ignores it.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-iwebbrowser2">IWebBrowser2</a>
