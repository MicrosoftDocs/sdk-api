---
UID: NF:printmanagerinterop.IPrintManagerInterop.ShowPrintUIForWindowAsync
title: IPrintManagerInterop::ShowPrintUIForWindowAsync
author: windows-sdk-content
description: Displays the UI for printing content for the specified window.
old-location: winrt\iprintmanagerinterop_showprintuiforwindowasync.htm
old-project: WinRT
ms.assetid: 2414279e-e1ef-48c7-87a1-a09ad367aec4
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IPrintManagerInterop interface [Windows Runtime],ShowPrintUIForWindowAsync method, IPrintManagerInterop.ShowPrintUIForWindowAsync, IPrintManagerInterop::ShowPrintUIForWindowAsync, ShowPrintUIForWindowAsync, ShowPrintUIForWindowAsync method [Windows Runtime], ShowPrintUIForWindowAsync method [Windows Runtime],IPrintManagerInterop interface, printmanagerinterop/IPrintManagerInterop::ShowPrintUIForWindowAsync, winrt.iprintmanagerinterop_showprintuiforwindowasync
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USER_POWER_POLICY, *PUSER_POWER_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - printmanagerinterop.h
api_name:
 - IPrintManagerInterop.ShowPrintUIForWindowAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>ShowPrintUIForWindowAsync</b> method to show the print UI for the specified window. The <b>ShowPrintUIForWindowAsync</b> method is equivalent to the <a href="https://msdn.microsoft.com/74a7b687-909d-42f2-bb58-83b5be474d9c">ShowPrintUIAsync</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/1786fda1-37e4-4ec5-94de-a1fc5b6732a2">IPrintManagerInterop</a>



<a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a>



<a href="https://msdn.microsoft.com/74a7b687-909d-42f2-bb58-83b5be474d9c">ShowPrintUIAsync</a>
 

 

