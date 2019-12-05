---
UID: NF:playtomanagerinterop.IPlayToManagerInterop.ShowPlayToUIForWindow
title: IPlayToManagerInterop::ShowPlayToUIForWindow (playtomanagerinterop.h)
description: Displays the Play To UI for the specified window.
old-location: winrt\iplaytomanagerinterop_showplaytouiforwindow.htm
tech.root: WinRT
ms.assetid: 106ddd95-06dd-479a-8350-39d791add469
ms.date: 12/05/2018
ms.keywords: IPlayToManagerInterop interface [Windows Runtime],ShowPlayToUIForWindow method, IPlayToManagerInterop.ShowPlayToUIForWindow, IPlayToManagerInterop::ShowPlayToUIForWindow, ShowPlayToUIForWindow, ShowPlayToUIForWindow method [Windows Runtime], ShowPlayToUIForWindow method [Windows Runtime],IPlayToManagerInterop interface, playtomanagerinterop/IPlayToManagerInterop::ShowPlayToUIForWindow, winrt.iplaytomanagerinterop_showplaytouiforwindow
ms.topic: method
f1_keywords:
- playtomanagerinterop/IPlayToManagerInterop.ShowPlayToUIForWindow
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- playtomanagerinterop.h
api_name:
- IPlayToManagerInterop.ShowPlayToUIForWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



You can use the <b>ShowPlayToUIForWindow</b> method to show the Play To UI for the specified window. The <b>ShowPlayToUIForWindow</b> method is equivalent to the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.media.playto.playtomanager.showplaytoui">ShowPlayToUI</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop">IPlayToManagerInterop</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.media.playto.playtomanager">PlayToManager</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.media.playto.playtomanager.showplaytoui">ShowPlayToUI</a>
 

 

