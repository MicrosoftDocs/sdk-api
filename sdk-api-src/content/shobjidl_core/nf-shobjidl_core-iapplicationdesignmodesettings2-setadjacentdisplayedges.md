---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetAdjacentDisplayEdges
title: IApplicationDesignModeSettings2::SetAdjacentDisplayEdges (shobjidl_core.h)
description: Sets whether the application window will be adjacent to the edge of the emulated display.
helpviewer_keywords: ["ADE_LEFT","ADE_NONE","ADE_RIGHT","IApplicationDesignModeSettings2 interface [Windows Shell]","SetAdjacentDisplayEdges method","IApplicationDesignModeSettings2.SetAdjacentDisplayEdges","IApplicationDesignModeSettings2::SetAdjacentDisplayEdges","SetAdjacentDisplayEdges","SetAdjacentDisplayEdges method [Windows Shell]","SetAdjacentDisplayEdges method [Windows Shell]","IApplicationDesignModeSettings2 interface","shell.IApplicationDesignModeSettings2_SetAdjacentDisplayEdges","shobjidl_core/IApplicationDesignModeSettings2::SetAdjacentDisplayEdges"]
old-location: shell\IApplicationDesignModeSettings2_SetAdjacentDisplayEdges.htm
tech.root: shell
ms.assetid: FD8B2436-1ADD-4371-AEB4-27EBDEC5BA04
ms.date: 12/05/2018
ms.keywords: ADE_LEFT, ADE_NONE, ADE_RIGHT, IApplicationDesignModeSettings2 interface [Windows Shell],SetAdjacentDisplayEdges method, IApplicationDesignModeSettings2.SetAdjacentDisplayEdges, IApplicationDesignModeSettings2::SetAdjacentDisplayEdges, SetAdjacentDisplayEdges, SetAdjacentDisplayEdges method [Windows Shell], SetAdjacentDisplayEdges method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetAdjacentDisplayEdges, shobjidl_core/IApplicationDesignModeSettings2::SetAdjacentDisplayEdges
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDesignModeSettings2::SetAdjacentDisplayEdges
 - shobjidl_core/IApplicationDesignModeSettings2::SetAdjacentDisplayEdges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - twinapi.dll
api_name:
 - IApplicationDesignModeSettings2.SetAdjacentDisplayEdges
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings">IApplicationDesignModeSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2">IApplicationDesignModeSettings2</a>