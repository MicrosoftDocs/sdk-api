---
UID: NF:shobjidl.IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop
title: IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop method
author: windows-driver-content
description: Indicates whether the provided window is on the currently active virtual desktop.
old-location: shell\ivirtualdesktopmanager_iswindowoncurrentvirtualdesktop.htm
old-project: shell
ms.assetid: CBC97CF4-0C88-4C68-A873-5A5962C5817D
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IVirtualDesktopManager, IVirtualDesktopManager interface [Windows Shell], IsWindowOnCurrentVirtualDesktop method, IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop, IsWindowOnCurrentVirtualDesktop method [Windows Shell], IsWindowOnCurrentVirtualDesktop method [Windows Shell], IVirtualDesktopManager interface, IsWindowOnCurrentVirtualDesktop,IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop, shell.ivirtualdesktopmanager_iswindowoncurrentvirtualdesktop, shobjidl/IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl.h
api_name:
-	IVirtualDesktopManager.IsWindowOnCurrentVirtualDesktop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IVirtualDesktopManager::IsWindowOnCurrentVirtualDesktop method


## -description


Indicates whether the provided window is on the currently active virtual desktop.


## -parameters




### -param topLevelWindow [in]

The window of interest.


### -param onCurrentDesktop [out]

<b>True</b> if the <i>topLevelWindow</i> is on the currently active virtual desktop, otherwise <b>false</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B95AC349-63E3-4A5A-A353-1C93486BB67A">IVirtualDesktopManager</a>
 

 

