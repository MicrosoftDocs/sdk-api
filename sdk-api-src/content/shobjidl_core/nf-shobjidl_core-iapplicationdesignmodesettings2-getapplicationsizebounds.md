---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.GetApplicationSizeBounds
title: IApplicationDesignModeSettings2::GetApplicationSizeBounds (shobjidl_core.h)
description: This methods retrieves the size bounds supported by the application.
helpviewer_keywords: ["GetApplicationSizeBounds","GetApplicationSizeBounds method [Windows Shell]","GetApplicationSizeBounds method [Windows Shell]","IApplicationDesignModeSettings2 interface","IApplicationDesignModeSettings2 interface [Windows Shell]","GetApplicationSizeBounds method","IApplicationDesignModeSettings2.GetApplicationSizeBounds","IApplicationDesignModeSettings2::GetApplicationSizeBounds","shell.IApplicationDesignModeSettings2_GetApplicationSizeBounds","shobjidl_core/IApplicationDesignModeSettings2::GetApplicationSizeBounds"]
old-location: shell\IApplicationDesignModeSettings2_GetApplicationSizeBounds.htm
tech.root: shell
ms.assetid: 7DFAFE5A-8F19-471C-9B09-43645F26F156
ms.date: 12/05/2018
ms.keywords: GetApplicationSizeBounds, GetApplicationSizeBounds method [Windows Shell], GetApplicationSizeBounds method [Windows Shell],IApplicationDesignModeSettings2 interface, IApplicationDesignModeSettings2 interface [Windows Shell],GetApplicationSizeBounds method, IApplicationDesignModeSettings2.GetApplicationSizeBounds, IApplicationDesignModeSettings2::GetApplicationSizeBounds, shell.IApplicationDesignModeSettings2_GetApplicationSizeBounds, shobjidl_core/IApplicationDesignModeSettings2::GetApplicationSizeBounds
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
 - IApplicationDesignModeSettings2::GetApplicationSizeBounds
 - shobjidl_core/IApplicationDesignModeSettings2::GetApplicationSizeBounds
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
 - IApplicationDesignModeSettings2.GetApplicationSizeBounds
---

# IApplicationDesignModeSettings2::GetApplicationSizeBounds


## -description

This methods retrieves the size bounds supported by the application.

## -parameters

### -param minApplicationSizePixels [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

When this method returns successfully, receives a pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that defines the minimum possible window size.

### -param maxApplicationSizePixels [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

When this method returns successfully, receives a pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that defines the maximum possible window size.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2">IApplicationDesignModeSettings2</a>