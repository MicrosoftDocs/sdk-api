---
UID: NF:shobjidl_core.IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop
title: IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop (shobjidl_core.h)
description: Indicates whether the provided window is on the currently active virtual desktop.
helpviewer_keywords: ["IVirtualDesktopManager interface [Windows Shell]","IsWindowOnCurrentVirtualDesktop method","IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop","IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop","IsWindowOnCurrentVirtualDesktop","IsWindowOnCurrentVirtualDesktop method [Windows Shell]","IsWindowOnCurrentVirtualDesktop method [Windows Shell]","IVirtualDesktopManager interface","shell.ivirtualdesktopmanager_iswindowoncurrentvirtualdesktop","shobjidl_core/IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop"]
old-location: shell\ivirtualdesktopmanager_iswindowoncurrentvirtualdesktop.htm
tech.root: shell
ms.assetid: CBC97CF4-0C88-4C68-A873-5A5962C5817D
ms.date: 12/05/2018
ms.keywords: IVirtualDesktopManager interface [Windows Shell],IsWindowOnCurrentVirtualDesktop method, IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop, IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop, IsWindowOnCurrentVirtualDesktop, IsWindowOnCurrentVirtualDesktop method [Windows Shell], IsWindowOnCurrentVirtualDesktop method [Windows Shell],IVirtualDesktopManager interface, shell.ivirtualdesktopmanager_iswindowoncurrentvirtualdesktop, shobjidl_core/IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop
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
 - IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop
 - shobjidl_core/IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop
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
 - IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop
---

# IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop


## -description

Indicates whether the provided window is on the currently active virtual desktop.

## -parameters

### -param topLevelWindow [in]

The window of interest.

### -param onCurrentDesktop [out]

<b>True</b> if the <i>topLevelWindow</i> is on the currently active virtual desktop, otherwise <b>false</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

[IVirtualDesktopManager](./nn-shobjidl_core-ivirtualdesktopmanager.md)