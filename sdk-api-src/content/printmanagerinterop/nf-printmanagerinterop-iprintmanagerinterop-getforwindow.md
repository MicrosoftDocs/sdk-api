---
UID: NF:printmanagerinterop.IPrintManagerInterop.GetForWindow
title: IPrintManagerInterop::GetForWindow
author: windows-sdk-content
description: Gets the PrintManager instance for the specified window.
old-location: winrt\iprintmanagerinterop_getforwindow.htm
tech.root: WinRT
ms.assetid: 8cbf37b6-6756-4399-aa6b-01eb63c8c6db
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Runtime], GetForWindow method [Windows Runtime],IPrintManagerInterop interface, IPrintManagerInterop interface [Windows Runtime],GetForWindow method, IPrintManagerInterop.GetForWindow, IPrintManagerInterop::GetForWindow, printmanagerinterop/IPrintManagerInterop::GetForWindow, winrt.iprintmanagerinterop_getforwindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - printmanagerinterop.h
api_name:
 - IPrintManagerInterop.GetForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintManagerInterop::GetForWindow


## -description


Gets the <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> instance for the specified window.


## -parameters




### -param appWindow [in]

The window to get the <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> instance for.


### -param riid [in]

The reference ID of the specified window.


### -param printManager [out, retval]

The <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> instance for the specified window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>GetForWindow</b> method to get the <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> for the specified window. The <b>GetForWindow</b> method is equivalent to the <a href="https://msdn.microsoft.com/0c973c56-8b35-4044-b9e1-36b7e05f02ed">GetForCurrentView</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/0c973c56-8b35-4044-b9e1-36b7e05f02ed">GetForCurrentView</a>



<a href="https://msdn.microsoft.com/1786fda1-37e4-4ec5-94de-a1fc5b6732a2">IPrintManagerInterop</a>



<a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a>
 

 

