---
UID: NF:shlobj_core.IShellIconOverlayManager.RefreshOverlayImages
title: IShellIconOverlayManager::RefreshOverlayImages (shlobj_core.h)
description: Refreshes the overlay cache, the image list, or both.
helpviewer_keywords: ["IShellIconOverlayManager interface [Windows Shell]","RefreshOverlayImages method","IShellIconOverlayManager.RefreshOverlayImages","IShellIconOverlayManager::RefreshOverlayImages","RefreshOverlayImages","RefreshOverlayImages method [Windows Shell]","RefreshOverlayImages method [Windows Shell]","IShellIconOverlayManager interface","SIOM_ICONINDEX","SIOM_OVERLAYINDEX","_win32_IShellIconOverlayManager_RefreshOverlayImages","shell.IShellIconOverlayManager_RefreshOverlayImages","shlobj_core/IShellIconOverlayManager::RefreshOverlayImages"]
old-location: shell\IShellIconOverlayManager_RefreshOverlayImages.htm
tech.root: shell
ms.assetid: 79b1e1c7-a008-4f68-88a2-379715167410
ms.date: 12/05/2018
ms.keywords: IShellIconOverlayManager interface [Windows Shell],RefreshOverlayImages method, IShellIconOverlayManager.RefreshOverlayImages, IShellIconOverlayManager::RefreshOverlayImages, RefreshOverlayImages, RefreshOverlayImages method [Windows Shell], RefreshOverlayImages method [Windows Shell],IShellIconOverlayManager interface, SIOM_ICONINDEX, SIOM_OVERLAYINDEX, _win32_IShellIconOverlayManager_RefreshOverlayImages, shell.IShellIconOverlayManager_RefreshOverlayImages, shlobj_core/IShellIconOverlayManager::RefreshOverlayImages
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellIconOverlayManager::RefreshOverlayImages
 - shlobj_core/IShellIconOverlayManager::RefreshOverlayImages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayManager.RefreshOverlayImages
---

# IShellIconOverlayManager::RefreshOverlayImages


## -description

Refreshes the overlay cache, the image list, or both.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Determines what to refresh. It can be a bitwise OR one of the following: 



#### SIOM_ICONINDEX

Reloads the icons into the image list.



#### SIOM_OVERLAYINDEX

Reloads the overlay cache.

## -returns

Type: <b>HRESULT</b>

This method always returns S_OK.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlaymanager">IShellIconOverlayManager</a>