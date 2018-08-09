---
UID: NF:playtomanagerinterop.IPlayToManagerInterop.ShowPlayToUIForWindow
title: IPlayToManagerInterop::ShowPlayToUIForWindow
author: windows-sdk-content
description: Displays the Play To UI for the specified window.
old-location: winrt\iplaytomanagerinterop_showplaytouiforwindow.htm
old-project: WinRT
ms.assetid: 106ddd95-06dd-479a-8350-39d791add469
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPlayToManagerInterop interface [Windows Runtime],ShowPlayToUIForWindow method, IPlayToManagerInterop.ShowPlayToUIForWindow, IPlayToManagerInterop::ShowPlayToUIForWindow, ShowPlayToUIForWindow, ShowPlayToUIForWindow method [Windows Runtime], ShowPlayToUIForWindow method [Windows Runtime],IPlayToManagerInterop interface, playtomanagerinterop/IPlayToManagerInterop::ShowPlayToUIForWindow, winrt.iplaytomanagerinterop_showplaytouiforwindow
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
 - IPlayToManagerInterop.ShowPlayToUIForWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPlayToManagerInterop::ShowPlayToUIForWindow


## -description


Displays the Play To UI for the specified window.


## -parameters




### -param appWindow [in]

The window to show the Play To UI  for.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>ShowPlayToUIForWindow</b> method to show the Play To UI for the specified window. The <b>ShowPlayToUIForWindow</b> method is equivalent to the <a href="https://msdn.microsoft.com/c1bb02b9-c719-4efe-bafe-d36b1703f0dc">ShowPlayToUI</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/e7a8df61-e5ae-4eff-a4eb-e0a5cdae3b7f">IPlayToManagerInterop</a>



<a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a>



<a href="https://msdn.microsoft.com/c1bb02b9-c719-4efe-bafe-d36b1703f0dc">ShowPlayToUI</a>
 

 

