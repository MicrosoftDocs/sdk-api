---
UID: NF:shobjidl_core.IExecuteCommand.SetShowWindow
title: IExecuteCommand::SetShowWindow (shobjidl_core.h)
author: windows-sdk-content
description: Sets the specified window's visual state.
old-location: shell\IExecuteCommand_SetShowWindow.htm
tech.root: shell
ms.assetid: 57ac201e-0680-4856-ab05-9f8b49aecd62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetShowWindow method, IExecuteCommand.SetShowWindow, IExecuteCommand::SetShowWindow, SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWDEFAULT, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, SetShowWindow, SetShowWindow method [Windows Shell], SetShowWindow method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetShowWindow, shell.IExecuteCommand_SetShowWindow, shobjidl_core/IExecuteCommand::SetShowWindow
ms.topic: method
f1_keywords:
- shobjidl_core/IExecuteCommand.SetShowWindow
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- shobjidl_core.h
api_name:
- IExecuteCommand.SetShowWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Sets the show state based on the information specified in the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure passed to the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function that started the application. An application should call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> with this flag to set the initial visual state of its main window.



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



