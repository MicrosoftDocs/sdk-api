---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetIsOnLockScreen
title: IApplicationDesignModeSettings2::SetIsOnLockScreen (shobjidl_core.h)
description: This method determines whether or not the application, in design mode, can display information on the Windows 8 lock screen.
helpviewer_keywords: ["IApplicationDesignModeSettings2 interface [Windows Shell]","SetIsOnLockScreen method","IApplicationDesignModeSettings2.SetIsOnLockScreen","IApplicationDesignModeSettings2::SetIsOnLockScreen","SetIsOnLockScreen","SetIsOnLockScreen method [Windows Shell]","SetIsOnLockScreen method [Windows Shell]","IApplicationDesignModeSettings2 interface","shell.IApplicationDesignModeSettings2_SetIsOnLockScreen","shobjidl_core/IApplicationDesignModeSettings2::SetIsOnLockScreen"]
old-location: shell\IApplicationDesignModeSettings2_SetIsOnLockScreen.htm
tech.root: shell
ms.assetid: 5BFBB0E4-2448-44B1-B2F3-68AB8392C3A4
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings2 interface [Windows Shell],SetIsOnLockScreen method, IApplicationDesignModeSettings2.SetIsOnLockScreen, IApplicationDesignModeSettings2::SetIsOnLockScreen, SetIsOnLockScreen, SetIsOnLockScreen method [Windows Shell], SetIsOnLockScreen method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetIsOnLockScreen, shobjidl_core/IApplicationDesignModeSettings2::SetIsOnLockScreen
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
 - IApplicationDesignModeSettings2::SetIsOnLockScreen
 - shobjidl_core/IApplicationDesignModeSettings2::SetIsOnLockScreen
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
 - IApplicationDesignModeSettings2.SetIsOnLockScreen
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2">IApplicationDesignModeSettings2</a>