---
UID: NF:playtomanagerinterop.IPlayToManagerInterop.GetForWindow
title: IPlayToManagerInterop::GetForWindow
author: windows-sdk-content
description: Gets the PlayToManager instance for the specified window.
old-location: winrt\iplaytomanagerinterop_getforwindow.htm
old-project: WinRT
ms.assetid: 444f0d68-a6ae-46de-aa97-d7d505c95948
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Runtime], GetForWindow method [Windows Runtime],IPlayToManagerInterop interface, IPlayToManagerInterop interface [Windows Runtime],GetForWindow method, IPlayToManagerInterop.GetForWindow, IPlayToManagerInterop::GetForWindow, playtomanagerinterop/IPlayToManagerInterop::GetForWindow, winrt.iplaytomanagerinterop_getforwindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - playtomanagerinterop.h
api_name:
 - IPlayToManagerInterop.GetForWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPlayToManagerInterop::GetForWindow


## -description


Gets the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for the specified window.


## -parameters




### -param appWindow [in]

The window to get the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for.


### -param riid [in]

The reference ID of the specified window.


### -param playToManager [out, retval]

The <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for the specified window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>GetForWindow</b> method to get the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> for the specified window. The <b>GetForWindow</b> method is equivalent to the <a href="https://msdn.microsoft.com/8b707202-fb49-4e3e-885c-a37d17211487">GetForCurrentView</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/8b707202-fb49-4e3e-885c-a37d17211487">GetForCurrentView</a>



<a href="https://msdn.microsoft.com/e7a8df61-e5ae-4eff-a4eb-e0a5cdae3b7f">IPlayToManagerInterop</a>



<a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a>
 

 

