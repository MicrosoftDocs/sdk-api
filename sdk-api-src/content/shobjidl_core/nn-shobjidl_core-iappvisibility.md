---
UID: NN:shobjidl_core.IAppVisibility
title: IAppVisibility (shobjidl_core.h)
description: Provides functionality to determine whether the display is showing Universal Windows Platform apps.
helpviewer_keywords: ["IAppVisibility","IAppVisibility interface [Windows Shell]","IAppVisibility interface [Windows Shell]","described","shell.IAppVisibility","shobjidl_core/IAppVisibility"]
old-location: shell\IAppVisibility.htm
tech.root: shell
ms.assetid: 89E26D36-3536-45F5-9396-83CCFB26890B
ms.date: 12/05/2018
ms.keywords: IAppVisibility, IAppVisibility interface [Windows Shell], IAppVisibility interface [Windows Shell],described, shell.IAppVisibility, shobjidl_core/IAppVisibility
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppVisibility
 - shobjidl_core/IAppVisibility
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAppVisibility
---

# IAppVisibility interface


## -description

Provides functionality to determine whether the display is showing Universal Windows Platform apps.

## -inheritance

The <b>IAppVisibility</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppVisibility</b> also has these types of members:

## -remarks

Use the <b>IAppVisibility</b> interface to determine when a display is showing Universal Windows Platform apps. This is useful for accessibility tools and other applications.

Use the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-islaunchervisible">IsLauncherVisible</a>  method to determine when  the Start screen is visible.

Don't implement the <b>IAppVisibility</b> interface. Instead, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function with <b>CLSID_AppVisibility</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents">IAppVisibilityEvents</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility">MONITOR_APP_VISIBILITY</a>
