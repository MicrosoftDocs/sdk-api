---
UID: NF:shobjidl_core.IDockingWindow.CloseDW
title: IDockingWindow::CloseDW
author: windows-driver-content
description: Notifies the docking window object that it is about to be removed from the frame. The docking window object should save any persistent information at this time.
old-location: shell\IDockingWindow_CloseDW.htm
old-project: shell
ms.assetid: 29e57436-cc8f-46e8-bc1a-b44bd803c4a8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CloseDW, CloseDW method [Windows Shell], CloseDW method [Windows Shell],IDockingWindow interface, IDockingWindow interface [Windows Shell],CloseDW method, IDockingWindow.CloseDW, IDockingWindow::CloseDW, _win32_IDockingWindow_CloseDW, shell.IDockingWindow_CloseDW, shobjidl_core/IDockingWindow::CloseDW
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IDockingWindow.CloseDW
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDockingWindow::CloseDW


## -description


Notifies the docking window object that it is about to be removed from the frame. The docking window object should save any persistent information at this time.


## -parameters




### -param dwReserved

Type: <b>DWORD</b>

Reserved. This parameter should always be zero.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>



<a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>



<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

