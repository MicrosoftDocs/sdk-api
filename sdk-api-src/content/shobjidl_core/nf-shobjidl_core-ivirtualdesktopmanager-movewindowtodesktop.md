---
UID: NF:shobjidl_core.IVirtualDesktopManager.MoveWindowToDesktop
title: IVirtualDesktopManager::MoveWindowToDesktop (shobjidl_core.h)
author: windows-sdk-content
description: Moves a window to the specified virtual desktop.
old-location: shell\ivirtualdesktopmanager_movewindowtodesktop.htm
tech.root: shell
ms.assetid: A8756361-E371-41C5-B3F5-BD99439878D9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVirtualDesktopManager interface [Windows Shell],MoveWindowToDesktop method, IVirtualDesktopManager.MoveWindowToDesktop, IVirtualDesktopManager::MoveWindowToDesktop, MoveWindowToDesktop, MoveWindowToDesktop method [Windows Shell], MoveWindowToDesktop method [Windows Shell],IVirtualDesktopManager interface, shell.ivirtualdesktopmanager_movewindowtodesktop, shobjidl_core/IVirtualDesktopManager::MoveWindowToDesktop
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IVirtualDesktopManager.MoveWindowToDesktop"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IVirtualDesktopManager.MoveWindowToDesktop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVirtualDesktopManager::MoveWindowToDesktop


## -description


Moves a window to the specified virtual desktop.


## -parameters




### -param topLevelWindow [in]

The window to move.


### -param desktopId [in]

The identifier of the virtual desktop to move the <i>topLeveLWindow</i> to. You can use <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ivirtualdesktopmanager-getwindowdesktopid">GetWindowDesktopId</a> to get a window's identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-ivirtualdesktopmanager">IVirtualDesktopManager</a>
 

 

