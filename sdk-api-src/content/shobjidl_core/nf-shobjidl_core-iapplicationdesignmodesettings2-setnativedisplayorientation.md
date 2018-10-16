---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetNativeDisplayOrientation
title: IApplicationDesignModeSettings2::SetNativeDisplayOrientation
author: windows-sdk-content
description: Sets the orientation of the emulated display for the design mode window.
old-location: shell\IApplicationDesignModeSettings2_SetNativeDisplayOrientation.htm
tech.root: shell
ms.assetid: 9473724C-3FD2-48D0-BCFA-EA148F0C4569
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IApplicationDesignModeSettings2 interface [Windows Shell],SetNativeDisplayOrientation method, IApplicationDesignModeSettings2.SetNativeDisplayOrientation, IApplicationDesignModeSettings2::SetNativeDisplayOrientation, NDO_LANDSCAPE, NDO_PORTRAIT, SetNativeDisplayOrientation, SetNativeDisplayOrientation method [Windows Shell], SetNativeDisplayOrientation method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetNativeDisplayOrientation, shobjidl_core/IApplicationDesignModeSettings2::SetNativeDisplayOrientation
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
 - IApplicationDesignModeSettings2.SetNativeDisplayOrientation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings2::SetNativeDisplayOrientation


## -description


Sets the orientation of the emulated display for the design mode window.


## -parameters




### -param nativeDisplayOrientation [in]

Type: <b>NATIVE_DISPLAY_ORIENTATION</b>

The native orientation of the display to emulate.



#### NDO_LANDSCAPE (0)

Landscape orientation, with the display width greater than the height.



#### NDO_PORTRAIT (1)

Portrait orientation, with the display height greater than the width.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1F630AFF-3C73-461C-AE41-D597F6FF42D8">IApplicationDesignModeSettings2</a>
 

 

