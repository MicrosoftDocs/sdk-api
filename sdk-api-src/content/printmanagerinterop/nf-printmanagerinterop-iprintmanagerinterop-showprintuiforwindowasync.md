---
UID: NF:printmanagerinterop.IPrintManagerInterop.ShowPrintUIForWindowAsync
title: IPrintManagerInterop::ShowPrintUIForWindowAsync (printmanagerinterop.h)
description: Displays the UI for printing content for the specified window.
helpviewer_keywords: ["IPrintManagerInterop interface [Windows Runtime]","ShowPrintUIForWindowAsync method","IPrintManagerInterop.ShowPrintUIForWindowAsync","IPrintManagerInterop::ShowPrintUIForWindowAsync","ShowPrintUIForWindowAsync","ShowPrintUIForWindowAsync method [Windows Runtime]","ShowPrintUIForWindowAsync method [Windows Runtime]","IPrintManagerInterop interface","printmanagerinterop/IPrintManagerInterop::ShowPrintUIForWindowAsync","winrt.iprintmanagerinterop_showprintuiforwindowasync"]
old-location: winrt\iprintmanagerinterop_showprintuiforwindowasync.htm
tech.root: WinRT
ms.assetid: 2414279e-e1ef-48c7-87a1-a09ad367aec4
ms.date: 12/05/2018
ms.keywords: IPrintManagerInterop interface [Windows Runtime],ShowPrintUIForWindowAsync method, IPrintManagerInterop.ShowPrintUIForWindowAsync, IPrintManagerInterop::ShowPrintUIForWindowAsync, ShowPrintUIForWindowAsync, ShowPrintUIForWindowAsync method [Windows Runtime], ShowPrintUIForWindowAsync method [Windows Runtime],IPrintManagerInterop interface, printmanagerinterop/IPrintManagerInterop::ShowPrintUIForWindowAsync, winrt.iprintmanagerinterop_showprintuiforwindowasync
req.header: printmanagerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Printmanagerinterop.idl
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
 - IPrintManagerInterop::ShowPrintUIForWindowAsync
 - printmanagerinterop/IPrintManagerInterop::ShowPrintUIForWindowAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - printmanagerinterop.h
api_name:
 - IPrintManagerInterop.ShowPrintUIForWindowAsync
---

# IPrintManagerInterop::ShowPrintUIForWindowAsync


## -description

Displays the UI for printing content for the specified window.

## -parameters

### -param appWindow [in]

The window to show the print UI  for.

### -param riid [in]

The reference ID of the specified window.

### -param asyncOperation [out, retval]

The asynchronous operation that reports completion.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the <b>ShowPrintUIForWindowAsync</b> method to show the print UI for the specified window. The <b>ShowPrintUIForWindowAsync</b> method is equivalent to the <a href="/uwp/api/windows.graphics.printing.printmanager.showprintuiasync">ShowPrintUIAsync</a> method, except that you supply a reference to a window from a multi-window Windows Store app.

## -see-also

<a href="/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop">IPrintManagerInterop</a>



<a href="/uwp/api/Windows.Graphics.Printing.PrintManager">PrintManager</a>



<a href="/uwp/api/windows.graphics.printing.printmanager.showprintuiasync">ShowPrintUIAsync</a>