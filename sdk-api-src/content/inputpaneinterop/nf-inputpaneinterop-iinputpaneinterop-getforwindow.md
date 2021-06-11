---
UID: NF:inputpaneinterop.IInputPaneInterop.GetForWindow
title: IInputPaneInterop::GetForWindow (inputpaneinterop.h)
description: Gets an instance of an InputPane object for the specified window.
helpviewer_keywords: ["GetForWindow","GetForWindow method [Windows Runtime]","GetForWindow method [Windows Runtime]","IInputPaneInterop interface","IInputPaneInterop interface [Windows Runtime]","GetForWindow method","IInputPaneInterop.GetForWindow","IInputPaneInterop::GetForWindow","inputpaneinterop/IInputPaneInterop::GetForWindow","winrt.iinputpaneinterop_getforwindow"]
old-location: winrt\iinputpaneinterop_getforwindow.htm
tech.root: WinRT
ms.assetid: 98A591F8-B85C-4400-9BA6-1B8F422C067B
ms.date: 12/05/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Runtime], GetForWindow method [Windows Runtime],IInputPaneInterop interface, IInputPaneInterop interface [Windows Runtime],GetForWindow method, IInputPaneInterop.GetForWindow, IInputPaneInterop::GetForWindow, inputpaneinterop/IInputPaneInterop::GetForWindow, winrt.iinputpaneinterop_getforwindow
req.header: inputpaneinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputPaneInterop.idl
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
 - IInputPaneInterop::GetForWindow
 - inputpaneinterop/IInputPaneInterop::GetForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inputpaneinterop.h
api_name:
 - IInputPaneInterop.GetForWindow
---

# IInputPaneInterop::GetForWindow

## -description

Gets an instance of an <a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> object for the specified window.

## -parameters

### -param appWindow [in]

The top-level ([GA_ROOT](../winuser/nf-winuser-getancestor.md)) window for which you want to get the <a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> object.

### -param riid [in]

The interface identifier for the interface that you want to get in the *inputPane* parameter. This value is typically **IID_IInputPane** or **IID_IInputPane2**, as defined in Windows.UI.ViewManagement.h.

### -param inputPane [out, retval]

The <a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> object for the window that the *appWindow* parameter specifies. This parameter is typically a pointer to an **IInputPane** or **IInputPane2** interface, as defined in Windows.UI.ViewManagement.idl.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

<a href="/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop">IInputPaneInterop</a>

<a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a>