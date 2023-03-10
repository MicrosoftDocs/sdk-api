---
UID: NN:corewindow.ICoreWindowInterop
title: ICoreWindowInterop (corewindow.h)
description: Enables apps to obtain the window handle of the window (CoreWindow) associated with this interface.
helpviewer_keywords: ["ICoreWindowInterop","ICoreWindowInterop interface [Windows Runtime]","ICoreWindowInterop interface [Windows Runtime]","described","corewindow/ICoreWindowInterop","winrt.icorewindowinterop"]
old-location: winrt\icorewindowinterop.htm
tech.root: WinRT
ms.assetid: 6928FA3A-C367-4C99-A67E-8ED0153D6349
ms.date: 12/05/2018
ms.keywords: ICoreWindowInterop, ICoreWindowInterop interface [Windows Runtime], ICoreWindowInterop interface [Windows Runtime],described, corewindow/ICoreWindowInterop, winrt.icorewindowinterop
req.header: corewindow.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICoreWindowInterop
 - corewindow/ICoreWindowInterop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - corewindow.h
api_name:
 - ICoreWindowInterop
---

# ICoreWindowInterop interface


## -description

Enables apps to obtain the window handle of the window (<a href="/uwp/api/windows.ui.core.corewindow">CoreWindow</a>) associated with this interface.

## -remarks

Windows Store apps can have multiple <a href="/uwp/api/windows.ui.core.corewindow">CoreWindow</a> instances. Each <b>CoreWindow</b> instance also has a native interface for accessing the underlying HWND, represented as an instance of <b>ICoreWindowInterop</b>.

## -see-also

<a href="/uwp/api/windows.ui.core.corewindow">CoreWindow</a>

