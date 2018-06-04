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

# IVirtualDesktopManager::MoveWindowToDesktop


## -description


Moves a window to the specified virtual desktop.


## -parameters




### -param topLevelWindow [in]

The window to move.


### -param desktopId [in]

The identifier of the virtual desktop to move the <i>topLeveLWindow</i> to. You can use <a href="https://msdn.microsoft.com/1A53C70F-6034-449D-832E-A563886F20E4">GetWindowDesktopId</a> to get a window's identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B95AC349-63E3-4A5A-A353-1C93486BB67A">IVirtualDesktopManager</a>
 

 

