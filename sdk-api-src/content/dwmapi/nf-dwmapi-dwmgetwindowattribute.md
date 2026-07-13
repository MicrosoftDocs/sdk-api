---
UID: NF:dwmapi.DwmGetWindowAttribute
title: DwmGetWindowAttribute function (dwmapi.h)
description: Retrieves the current value of a specified Desktop Window Manager (DWM) attribute applied to a window.
helpviewer_keywords: ["DwmGetWindowAttribute","DwmGetWindowAttribute function [Desktop Window Manager]","_udwm_dwmgetwindowattribute","_udwm_dwmgetwindowattribute_cpp","dwm.dwmgetwindowattribute","dwmapi/DwmGetWindowAttribute","winui._udwm_dwmgetwindowattribute"]
old-location: dwm\dwmgetwindowattribute.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmgetwindowattribute.htm
ms.date: 05/30/2019
ms.keywords: DwmGetWindowAttribute, DwmGetWindowAttribute function [Desktop Window Manager], _udwm_dwmgetwindowattribute, _udwm_dwmgetwindowattribute_cpp, dwm.dwmgetwindowattribute, dwmapi/DwmGetWindowAttribute, winui._udwm_dwmgetwindowattribute
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DwmGetWindowAttribute
 - dwmapi/DwmGetWindowAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
 - Dwmapi.dll
api_name:
 - DwmGetWindowAttribute
---

# DwmGetWindowAttribute function


## -description

Retrieves the current value of a specified Desktop Window Manager (DWM) attribute applied to a window. For programming guidance, and code examples, see [Controlling non-client region rendering](/windows/desktop/dwm/composition-ovw#controlling-non-client-region-rendering).

## -parameters

### -param hwnd [in]

The handle to the window from which the attribute value is to be retrieved.

### -param dwAttribute [in]

A flag describing which value to retrieve, specified as a value of the [DWMWINDOWATTRIBUTE](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) enumeration. This parameter specifies which attribute to retrieve, and the *pvAttribute* parameter points to an object into which the attribute value is retrieved.

### -param pvAttribute [out]

A pointer to a value which, when this function returns successfully, receives the current value of the attribute. The type of the retrieved value depends on the value of the *dwAttribute* parameter. The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter.

### -param cbAttribute [in]

The size, in bytes, of the attribute value being received via the *pvAttribute* parameter. The type of the retrieved value, and therefore its size in bytes, depends on the value of the *dwAttribute* parameter.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -see-also

* [DwmSetWindowAttribute function](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
* [Enable and control DWM composition](/windows/desktop/dwm/composition-ovw)

