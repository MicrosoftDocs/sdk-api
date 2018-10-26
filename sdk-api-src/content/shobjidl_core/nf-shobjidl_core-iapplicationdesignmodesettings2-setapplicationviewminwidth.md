---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetApplicationViewMinWidth
title: IApplicationDesignModeSettings2::SetApplicationViewMinWidth
author: windows-sdk-content
description: Sets the desired minimum width of the application design mode window.
old-location: shell\IApplicationDesignModeSettings2_SetApplicationViewMinWidth.htm
tech.root: shell
ms.assetid: 6132E0B9-E2B9-4768-909A-9D93A3F3A11C
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: AVMW_320, AVMW_500, AVMW_DEFAULT, IApplicationDesignModeSettings2 interface [Windows Shell],SetApplicationViewMinWidth method, IApplicationDesignModeSettings2.SetApplicationViewMinWidth, IApplicationDesignModeSettings2::SetApplicationViewMinWidth, SetApplicationViewMinWidth, SetApplicationViewMinWidth method [Windows Shell], SetApplicationViewMinWidth method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetApplicationViewMinWidth, shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewMinWidth
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
 - IApplicationDesignModeSettings2.SetApplicationViewMinWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings2::SetApplicationViewMinWidth


## -description


Sets the desired minimum width of the application design mode window.


## -parameters




### -param viewMinWidth [in]

Type: <b>APPLICATION_VIEW_MIN_WIDTH</b>

The minimum width value.



#### AVMW_DEFAULT (0)

Uses the default minimum width.



#### AVMW_320 (1)

Sets the minimum width at 320 pixels.



#### AVMW_500 (2)

Sets the minimum width at 500 pixels.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1F630AFF-3C73-461C-AE41-D597F6FF42D8">IApplicationDesignModeSettings2</a>
 

 

