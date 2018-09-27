---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetIsOnLockScreen
title: IApplicationDesignModeSettings2::SetIsOnLockScreen
author: windows-sdk-content
description: This method determines whether or not the application, in design mode, can display information on the Windows 8 lock screen.
old-location: shell\IApplicationDesignModeSettings2_SetIsOnLockScreen.htm
tech.root: shell
ms.assetid: 5BFBB0E4-2448-44B1-B2F3-68AB8392C3A4
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IApplicationDesignModeSettings2 interface [Windows Shell],SetIsOnLockScreen method, IApplicationDesignModeSettings2.SetIsOnLockScreen, IApplicationDesignModeSettings2::SetIsOnLockScreen, SetIsOnLockScreen, SetIsOnLockScreen method [Windows Shell], SetIsOnLockScreen method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetIsOnLockScreen, shobjidl_core/IApplicationDesignModeSettings2::SetIsOnLockScreen
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
 - IApplicationDesignModeSettings2.SetIsOnLockScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings2::SetIsOnLockScreen


## -description


This method determines whether or not the application, in design mode, can display information on the Windows 8 lock screen.


## -parameters




### -param isOnLockScreen [in]

Type: <b>BOOL</b>

When set to <b>TRUE</b>, the application will display information on the lock screen. When set to <b>FALSE</b>, information will not be displayed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1F630AFF-3C73-461C-AE41-D597F6FF42D8">IApplicationDesignModeSettings2</a>
 

 

