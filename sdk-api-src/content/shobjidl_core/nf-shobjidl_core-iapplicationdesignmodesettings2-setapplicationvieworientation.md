---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetApplicationViewOrientation
title: IApplicationDesignModeSettings2::SetApplicationViewOrientation
author: windows-sdk-content
description: Sets the window orientation used for the design mode window.
old-location: shell\IApplicationDesignModeSettings2_SetApplicationViewOrientation.htm
tech.root: shell
ms.assetid: FCD2FDFD-1058-45D6-B9D5-A4B845CF80AA
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IApplicationDesignModeSettings2 interface [Windows Shell],SetApplicationViewOrientation method, IApplicationDesignModeSettings2.SetApplicationViewOrientation, IApplicationDesignModeSettings2::SetApplicationViewOrientation, SetApplicationViewOrientation, SetApplicationViewOrientation method [Windows Shell], SetApplicationViewOrientation method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetApplicationViewOrientation, shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewOrientation
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
 - IApplicationDesignModeSettings2.SetApplicationViewOrientation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings2::SetApplicationViewOrientation


## -description


Sets the window orientation used for the design mode window.


## -parameters




### -param viewOrientation [in]

Type: <b><a href="https://msdn.microsoft.com/6E14D892-09E3-46F4-84AD-991996431FB2">APPLICATION_VIEW_ORIENTATION</a></b>

The orientation of the design mode window to use. Either <b>AVO_LANDSCAPE</b> or <b>AVO_PORTRAIT</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1F630AFF-3C73-461C-AE41-D597F6FF42D8">IApplicationDesignModeSettings2</a>
 

 

