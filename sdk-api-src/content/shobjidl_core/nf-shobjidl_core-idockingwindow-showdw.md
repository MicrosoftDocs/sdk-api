---
UID: NF:shobjidl_core.IDockingWindow.ShowDW
title: IDockingWindow::ShowDW
author: windows-sdk-content
description: Instructs the docking window object to show or hide itself.
old-location: shell\IDockingWindow_ShowDW.htm
old-project: shell
ms.assetid: c33031d4-f9f4-4210-93be-963e5f299408
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IDockingWindow interface [Windows Shell],ShowDW method, IDockingWindow.ShowDW, IDockingWindow::ShowDW, ShowDW, ShowDW method [Windows Shell], ShowDW method [Windows Shell],IDockingWindow interface, _win32_IDockingWindow_ShowDW, shell.IDockingWindow_ShowDW, shobjidl_core/IDockingWindow::ShowDW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDockingWindow.ShowDW
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDockingWindow::ShowDW


## -description


Instructs the docking window object to show or hide itself.


## -parameters




### -param fShow






#### - bShow

Type: <b>BOOL</b>

<b>TRUE</b> if the docking window object should show its window. <b>FALSE</b> if the docking window object should hide its window and return its border space by calling <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a> with zero values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>



<a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>



<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

