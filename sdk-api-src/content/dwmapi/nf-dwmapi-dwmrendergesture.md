---
UID: NF:dwmapi.DwmRenderGesture
title: DwmRenderGesture function (dwmapi.h)
description: Notifies Desktop Window Manager (DWM) that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.
helpviewer_keywords: ["DwmRenderGesture","DwmRenderGesture function [Desktop Window Manager]","dwm.dwmrendergesture","dwmapi/DwmRenderGesture"]
old-location: dwm\dwmrendergesture.htm
tech.root: dwm
ms.assetid: 2daad062-dd7f-4a0b-a31e-134980f5bebd
ms.date: 12/05/2018
ms.keywords: DwmRenderGesture, DwmRenderGesture function [Desktop Window Manager], dwm.dwmrendergesture, dwmapi/DwmRenderGesture
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmRenderGesture
 - dwmapi/DwmRenderGesture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - API-MS-Win-dwmapi-l1-1-0.dll
 - Ext-Ms-Win-DwmAPI-Ext-L1-1-0.dll
api_name:
 - DwmRenderGesture
---

# DwmRenderGesture function


## -description

Notifies Desktop Window Manager (DWM) that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.

## -parameters

### -param gt [in]

The type of gesture, specified as one of the <a href="/windows/desktop/api/dwmapi/ne-dwmapi-gesture_type">GESTURE_TYPE</a> values.

### -param cContacts [in]

The number of contact points.

### -param pdwPointerID [in]

The pointer ID.

### -param pPoints [in]

The points.