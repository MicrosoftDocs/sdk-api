---
UID: NF:shlobj_core.IShellIconOverlayManager.RefreshOverlayImages
title: IShellIconOverlayManager::RefreshOverlayImages
author: windows-sdk-content
description: Refreshes the overlay cache, the image list, or both.
old-location: shell\IShellIconOverlayManager_RefreshOverlayImages.htm
tech.root: shell
ms.assetid: 79b1e1c7-a008-4f68-88a2-379715167410
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IShellIconOverlayManager interface [Windows Shell],RefreshOverlayImages method, IShellIconOverlayManager.RefreshOverlayImages, IShellIconOverlayManager::RefreshOverlayImages, RefreshOverlayImages, RefreshOverlayImages method [Windows Shell], RefreshOverlayImages method [Windows Shell],IShellIconOverlayManager interface, SIOM_ICONINDEX, SIOM_OVERLAYINDEX, _win32_IShellIconOverlayManager_RefreshOverlayImages, shell.IShellIconOverlayManager_RefreshOverlayImages, shlobj_core/IShellIconOverlayManager::RefreshOverlayImages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayManager.RefreshOverlayImages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a>



<a href="https://msdn.microsoft.com/769c3b0b-ece4-4406-a76c-cabc37901351">IShellIconOverlayManager</a>
 

 

