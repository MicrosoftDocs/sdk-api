---
UID: NF:printmanagerinterop.IPrintManagerInterop.GetForWindow
title: IPrintManagerInterop::GetForWindow (printmanagerinterop.h)
description: Gets the PrintManager instance for the specified window.
helpviewer_keywords: ["GetForWindow","GetForWindow method [Windows Runtime]","GetForWindow method [Windows Runtime]","IPrintManagerInterop interface","IPrintManagerInterop interface [Windows Runtime]","GetForWindow method","IPrintManagerInterop.GetForWindow","IPrintManagerInterop::GetForWindow","printmanagerinterop/IPrintManagerInterop::GetForWindow","winrt.iprintmanagerinterop_getforwindow"]
old-location: winrt\iprintmanagerinterop_getforwindow.htm
tech.root: WinRT
ms.assetid: 8cbf37b6-6756-4399-aa6b-01eb63c8c6db
ms.date: 12/05/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Runtime], GetForWindow method [Windows Runtime],IPrintManagerInterop interface, IPrintManagerInterop interface [Windows Runtime],GetForWindow method, IPrintManagerInterop.GetForWindow, IPrintManagerInterop::GetForWindow, printmanagerinterop/IPrintManagerInterop::GetForWindow, winrt.iprintmanagerinterop_getforwindow
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
 - IPrintManagerInterop::GetForWindow
 - printmanagerinterop/IPrintManagerInterop::GetForWindow
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
 - IPrintManagerInterop.GetForWindow
---

# IPrintManagerInterop::GetForWindow


## -description

Gets the <a href="/uwp/api/Windows.Graphics.Printing.PrintManager">PrintManager</a> instance for the specified window.

## -parameters

### -param appWindow [in]

The window to get the <a href="/uwp/api/Windows.Graphics.Printing.PrintManager">PrintManager</a> instance for.

### -param riid [in]

The reference ID of the specified window.

### -param printManager [out, retval]

The <a href="/uwp/api/Windows.Graphics.Printing.PrintManager">PrintManager</a> instance for the specified window.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the <b>GetForWindow</b> method to get the <a href="/uwp/api/Windows.Graphics.Printing.PrintManager">PrintManager</a> for the specified window. The <b>GetForWindow</b> method is equivalent to the <a href="/uwp/api/windows.graphics.printing.printmanager.getforcurrentview">GetForCurrentView</a> method, except that you supply a reference to a window from a multi-window Windows Store app.

## -see-also

<a href="/uwp/api/windows.graphics.printing.printmanager.getforcurrentview">GetForCurrentView</a>



<a href="/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop">IPrintManagerInterop</a>



<a href="/uwp/api/Windows.Graphics.Printing.PrintManager">PrintManager</a>