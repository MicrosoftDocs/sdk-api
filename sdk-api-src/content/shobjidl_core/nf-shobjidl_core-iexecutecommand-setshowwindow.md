---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IExecuteCommand::SetShowWindow


## -description


Sets the specified window's visual state.


## -parameters




### -param nShow [in]

Type: <b>int</b>

One of the following flags to indicate how the window is to be shown.



#### SW_HIDE

Hides the window and activates another window.



#### SW_MAXIMIZE

Maximizes the specified window.



#### SW_MINIMIZE

Minimizes the specified window and activates the next top-level window in the z-order.



#### SW_RESTORE

Activates and displays the window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when restoring a minimized window.



#### SW_SHOW

Activates the window and displays it in its current size and position.



#### SW_SHOWDEFAULT

Sets the show state based on the information specified in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function that started the application. An application should call <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a> with this flag to set the initial visual state of its main window.



#### SW_SHOWMAXIMIZED

Activates the window and displays it as a maximized window.



#### SW_SHOWMINIMIZED

Activates the window and displays it as a minimized window.



#### SW_SHOWMINNOACTIVE

Displays the window as a minimized window. The active window remains active.



#### SW_SHOWNA

Displays the window in its current state. The active window remains active.



#### SW_SHOWNOACTIVATE

Displays a window in its most recent size and position. The active window remains active.



#### SW_SHOWNORMAL

Default state. Activates and displays a window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when it displays the window for the first time.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



