---
UID: NF:shobjidl_core.IVirtualDesktopManager.MoveWindowToDesktop
title: IVirtualDesktopManager::MoveWindowToDesktop (shobjidl_core.h)
description: Moves a window to the specified virtual desktop.
helpviewer_keywords: ["IVirtualDesktopManager interface [Windows Shell]","MoveWindowToDesktop method","IVirtualDesktopManager.MoveWindowToDesktop","IVirtualDesktopManager::MoveWindowToDesktop","MoveWindowToDesktop","MoveWindowToDesktop method [Windows Shell]","MoveWindowToDesktop method [Windows Shell]","IVirtualDesktopManager interface","shell.ivirtualdesktopmanager_movewindowtodesktop","shobjidl_core/IVirtualDesktopManager::MoveWindowToDesktop"]
old-location: shell\ivirtualdesktopmanager_movewindowtodesktop.htm
tech.root: shell
ms.assetid: A8756361-E371-41C5-B3F5-BD99439878D9
ms.date: 12/05/2018
ms.keywords: IVirtualDesktopManager interface [Windows Shell],MoveWindowToDesktop method, IVirtualDesktopManager.MoveWindowToDesktop, IVirtualDesktopManager::MoveWindowToDesktop, MoveWindowToDesktop, MoveWindowToDesktop method [Windows Shell], MoveWindowToDesktop method [Windows Shell],IVirtualDesktopManager interface, shell.ivirtualdesktopmanager_movewindowtodesktop, shobjidl_core/IVirtualDesktopManager::MoveWindowToDesktop
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IVirtualDesktopManager::MoveWindowToDesktop
 - shobjidl_core/IVirtualDesktopManager::MoveWindowToDesktop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IVirtualDesktopManager.MoveWindowToDesktop
---

# IVirtualDesktopManager::MoveWindowToDesktop


## -description

Moves a window to the specified virtual desktop.

## -parameters

### -param topLevelWindow [in]

The window to move.

### -param desktopId [in]

The identifier of the virtual desktop to move the [GetWindowDesktopId](./nf-shobjidl_core-ivirtualdesktopmanager-getwindowdesktopid.md) to get a window's identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

[IVirtualDesktopManager](./nn-shobjidl_core-ivirtualdesktopmanager.md)