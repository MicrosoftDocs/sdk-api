---
UID: NF:shobjidl_core.IApplicationDesignModeSettings2.SetApplicationViewOrientation
title: IApplicationDesignModeSettings2::SetApplicationViewOrientation (shobjidl_core.h)
description: Sets the window orientation used for the design mode window.
helpviewer_keywords: ["IApplicationDesignModeSettings2 interface [Windows Shell]","SetApplicationViewOrientation method","IApplicationDesignModeSettings2.SetApplicationViewOrientation","IApplicationDesignModeSettings2::SetApplicationViewOrientation","SetApplicationViewOrientation","SetApplicationViewOrientation method [Windows Shell]","SetApplicationViewOrientation method [Windows Shell]","IApplicationDesignModeSettings2 interface","shell.IApplicationDesignModeSettings2_SetApplicationViewOrientation","shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewOrientation"]
old-location: shell\IApplicationDesignModeSettings2_SetApplicationViewOrientation.htm
tech.root: shell
ms.assetid: FCD2FDFD-1058-45D6-B9D5-A4B845CF80AA
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings2 interface [Windows Shell],SetApplicationViewOrientation method, IApplicationDesignModeSettings2.SetApplicationViewOrientation, IApplicationDesignModeSettings2::SetApplicationViewOrientation, SetApplicationViewOrientation, SetApplicationViewOrientation method [Windows Shell], SetApplicationViewOrientation method [Windows Shell],IApplicationDesignModeSettings2 interface, shell.IApplicationDesignModeSettings2_SetApplicationViewOrientation, shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewOrientation
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
 - IApplicationDesignModeSettings2::SetApplicationViewOrientation
 - shobjidl_core/IApplicationDesignModeSettings2::SetApplicationViewOrientation
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
 - IApplicationDesignModeSettings2.SetApplicationViewOrientation
---

# IApplicationDesignModeSettings2::SetApplicationViewOrientation


## -description

Sets the window orientation used for the design mode window.

## -parameters

### -param viewOrientation [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_orientation">APPLICATION_VIEW_ORIENTATION</a></b>

The orientation of the design mode window to use. Either <b>AVO_LANDSCAPE</b> or <b>AVO_PORTRAIT</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2">IApplicationDesignModeSettings2</a>