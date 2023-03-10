---
UID: NF:playtomanagerinterop.IPlayToManagerInterop.GetForWindow
title: IPlayToManagerInterop::GetForWindow (playtomanagerinterop.h)
description: Gets the PlayToManager instance for the specified window.
helpviewer_keywords: ["GetForWindow","GetForWindow method [Windows Runtime]","GetForWindow method [Windows Runtime]","IPlayToManagerInterop interface","IPlayToManagerInterop interface [Windows Runtime]","GetForWindow method","IPlayToManagerInterop.GetForWindow","IPlayToManagerInterop::GetForWindow","playtomanagerinterop/IPlayToManagerInterop::GetForWindow","winrt.iplaytomanagerinterop_getforwindow"]
old-location: winrt\iplaytomanagerinterop_getforwindow.htm
tech.root: WinRT
ms.assetid: 444f0d68-a6ae-46de-aa97-d7d505c95948
ms.date: 12/05/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Runtime], GetForWindow method [Windows Runtime],IPlayToManagerInterop interface, IPlayToManagerInterop interface [Windows Runtime],GetForWindow method, IPlayToManagerInterop.GetForWindow, IPlayToManagerInterop::GetForWindow, playtomanagerinterop/IPlayToManagerInterop::GetForWindow, winrt.iplaytomanagerinterop_getforwindow
req.header: playtomanagerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Playtomanagerinterop.idl
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
 - IPlayToManagerInterop::GetForWindow
 - playtomanagerinterop/IPlayToManagerInterop::GetForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - playtomanagerinterop.h
api_name:
 - IPlayToManagerInterop.GetForWindow
---

# IPlayToManagerInterop::GetForWindow


## -description

Gets the <a href="/uwp/api/windows.media.playto.playtomanager">PlayToManager</a> instance for the specified window.

## -parameters

### -param appWindow [in]

The window to get the <a href="/uwp/api/windows.media.playto.playtomanager">PlayToManager</a> instance for.

### -param riid [in]

The reference ID of the specified window.

### -param playToManager [out, retval]

The <a href="/uwp/api/windows.media.playto.playtomanager">PlayToManager</a> instance for the specified window.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the <b>GetForWindow</b> method to get the <a href="/uwp/api/windows.media.playto.playtomanager">PlayToManager</a> for the specified window. The <b>GetForWindow</b> method is equivalent to the <a href="/uwp/api/windows.graphics.printing.printmanager.getforcurrentview">GetForCurrentView</a> method, except that you supply a reference to a window from a multi-window Windows Store app.

## -see-also

<a href="/uwp/api/windows.graphics.printing.printmanager.getforcurrentview">GetForCurrentView</a>



<a href="/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop">IPlayToManagerInterop</a>



<a href="/uwp/api/windows.media.playto.playtomanager">PlayToManager</a>