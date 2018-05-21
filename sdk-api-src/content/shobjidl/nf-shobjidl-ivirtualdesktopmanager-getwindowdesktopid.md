---
UID: NF:shobjidl.IVirtualDesktopManager.GetWindowDesktopId
title: IVirtualDesktopManager::GetWindowDesktopId
author: windows-driver-content
description: Gets the identifier for the virtual desktop hosting the provided top-level window.
old-location: shell\ivirtualdesktopmanager_getwindowdesktopid.htm
old-project: shell
ms.assetid: 1A53C70F-6034-449D-832E-A563886F20E4
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetWindowDesktopId, GetWindowDesktopId method [Windows Shell], GetWindowDesktopId method [Windows Shell],IVirtualDesktopManager interface, IVirtualDesktopManager interface [Windows Shell],GetWindowDesktopId method, IVirtualDesktopManager.GetWindowDesktopId, IVirtualDesktopManager::GetWindowDesktopId, shell.ivirtualdesktopmanager_getwindowdesktopid, shobjidl/IVirtualDesktopManager::GetWindowDesktopId
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
-	IVirtualDesktopManager.GetWindowDesktopId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IVirtualDesktopManager::GetWindowDesktopId


## -description


Gets the identifier for the virtual desktop hosting the provided top-level window.


## -parameters




### -param topLevelWindow [in]

The top level window for the virtual desktop you are interested in.


### -param desktopId [out]

The identifier for the virtual desktop hosting the <i>topLevelWindow</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B95AC349-63E3-4A5A-A353-1C93486BB67A">IVirtualDesktopManager</a>
 

 

