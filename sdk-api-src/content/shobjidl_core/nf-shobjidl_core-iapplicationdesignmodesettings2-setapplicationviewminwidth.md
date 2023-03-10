---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetApplicationViewMinWidth
title: IApplicationDesignModeSettings2::SetApplicationViewMinWidth (shobjidl_core.h)
description: Sets the desired minimum width of the application design mode window.
helpviewer_keywords: ["AVMW_320","AVMW_500","AVMW_DEFAULT","IApplicationDesignModeSettings2 interface [Windows Shell]","SetApplicationViewMinWidth method","IApplicationDesignModeSettings2.SetApplicationViewMinWidth","IApplicationDesignModeSettings2::SetApplicationViewMinWidth","SetApplicationViewMinWidth","SetApplicationViewMinWidth method [Windows Shell]","SetApplicationViewMinWidth method [Windows Shell]","IApplicationDesignModeSettings2 interface","shell.IApplicationDesignModeSettings2_SetApplicationViewMinWidth","shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewMinWidth"]
old-location: shell\IApplicationDesignModeSettings2_SetApplicationViewMinWidth.htm
tech.root: shell
ms.assetid: 6132E0B9-E2B9-4768-909A-9D93A3F3A11C
ms.date: 12/05/2018
ms.keywords: AVMW_320, AVMW_500, AVMW_DEFAULT, IApplicationDesignModeSettings2 interface [Windows Shell],SetApplicationViewMinWidth method, IApplicationDesignModeSettings2.SetApplicationViewMinWidth, IApplicationDesignModeSettings2::SetApplicationViewMinWidth, SetApplicationViewMinWidth, SetApplicationViewMinWidth method [Windows Shell], SetApplicationViewMinWidth method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetApplicationViewMinWidth, shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewMinWidth
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
 - IApplicationDesignModeSettings2::SetApplicationViewMinWidth
 - shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewMinWidth
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
 - IApplicationDesignModeSettings2.SetApplicationViewMinWidth
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2">IApplicationDesignModeSettings2</a>