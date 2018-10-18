---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetAdjacentDisplayEdges
title: IApplicationDesignModeSettings2::SetAdjacentDisplayEdges
author: windows-sdk-content
description: Sets whether the application window will be adjacent to the edge of the emulated display.
old-location: shell\IApplicationDesignModeSettings2_SetAdjacentDisplayEdges.htm
tech.root: shell
ms.assetid: FD8B2436-1ADD-4371-AEB4-27EBDEC5BA04
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ADE_LEFT, ADE_NONE, ADE_RIGHT, IApplicationDesignModeSettings2 interface [Windows Shell],SetAdjacentDisplayEdges method, IApplicationDesignModeSettings2.SetAdjacentDisplayEdges, IApplicationDesignModeSettings2::SetAdjacentDisplayEdges, SetAdjacentDisplayEdges, SetAdjacentDisplayEdges method [Windows Shell], SetAdjacentDisplayEdges method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetAdjacentDisplayEdges, shobjidl_core/IApplicationDesignModeSettings2::SetAdjacentDisplayEdges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Twinapi.lib
req.dll: Twinapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - twinapi.dll
api_name:
 - IApplicationDesignModeSettings2.SetAdjacentDisplayEdges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings2::SetAdjacentDisplayEdges


## -description


Sets whether the application window will be  adjacent to the edge of the emulated display.


## -parameters




### -param adjacentDisplayEdges [in]

Type: <b>ADJACENT_DISPLAY_EDGES</b>

The edge which should be adjacent.



#### ADE_NONE (0x0)

The widow will not be adjacent to either edge.



#### ADE_LEFT (0x1)

the left edge of the window will be adjacent.



#### ADE_RIGHT (0x2)

The right edge of the window will be adjacent.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>



<a href="https://msdn.microsoft.com/1F630AFF-3C73-461C-AE41-D597F6FF42D8">IApplicationDesignModeSettings2</a>
 

 

