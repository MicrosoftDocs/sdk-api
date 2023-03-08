---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.GetApplicationViewOrientation
title: IApplicationDesignModeSettings2::GetApplicationViewOrientation (shobjidl_core.h)
description: Gets the orientation of the application design mode window.
helpviewer_keywords: ["GetApplicationViewOrientation","GetApplicationViewOrientation method [Windows Shell]","GetApplicationViewOrientation method [Windows Shell]","IApplicationDesignModeSettings2 interface","IApplicationDesignModeSettings2 interface [Windows Shell]","GetApplicationViewOrientation method","IApplicationDesignModeSettings2.GetApplicationViewOrientation","IApplicationDesignModeSettings2::GetApplicationViewOrientation","shell.IApplicationDesignModeSettings2_GetApplicationViewOrientation","shobjidl_core/IApplicationDesignModeSettings2::GetApplicationViewOrientation"]
old-location: shell\IApplicationDesignModeSettings2_GetApplicationViewOrientation.htm
tech.root: shell
ms.assetid: D6DF8432-7D37-4D39-9E08-2F5B874A0BCB
ms.date: 12/05/2018
ms.keywords: GetApplicationViewOrientation, GetApplicationViewOrientation method [Windows Shell], GetApplicationViewOrientation method [Windows Shell],IApplicationDesignModeSettings2 interface, IApplicationDesignModeSettings2 interface [Windows Shell],GetApplicationViewOrientation method, IApplicationDesignModeSettings2.GetApplicationViewOrientation, IApplicationDesignModeSettings2::GetApplicationViewOrientation, shell.IApplicationDesignModeSettings2_GetApplicationViewOrientation, shobjidl_core/IApplicationDesignModeSettings2::GetApplicationViewOrientation
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
 - IApplicationDesignModeSettings2::GetApplicationViewOrientation
 - shobjidl_core/IApplicationDesignModeSettings2::GetApplicationViewOrientation
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
 - IApplicationDesignModeSettings2.GetApplicationViewOrientation
---

# IApplicationDesignModeSettings2::GetApplicationViewOrientation


## -description

Gets the orientation of the application design mode window.

## -parameters

### -param applicationSizePixels

Type: <b>SIZE</b>

The application window size.

### -param viewOrientation [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_orientation">APPLICATION_VIEW_ORIENTATION</a>*</b>

When this method returns successfully, receives a pointer to an  <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_orientation">APPLICATION_VIEW_ORIENTATION</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2">IApplicationDesignModeSettings2</a>