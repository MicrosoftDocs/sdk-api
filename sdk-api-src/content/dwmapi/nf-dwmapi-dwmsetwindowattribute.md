---
UID: NF:dwmapi.DwmSetWindowAttribute
title: DwmSetWindowAttribute function (dwmapi.h)
description: Sets the value of Desktop Window Manager (DWM) non-client rendering attributes for a window.
helpviewer_keywords: ["DwmSetWindowAttribute","DwmSetWindowAttribute function [Desktop Window Manager]","_udwm_dwmsetwindowattribute","_udwm_dwmsetwindowattribute_cpp","dwm.dwmsetwindowattribute","dwmapi/DwmSetWindowAttribute","winui._udwm_dwmsetwindowattribute"]
old-location: dwm\dwmsetwindowattribute.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmsetwindowattribute.htm
ms.date: 05/30/2019
ms.keywords: DwmSetWindowAttribute, DwmSetWindowAttribute function [Desktop Window Manager], _udwm_dwmsetwindowattribute, _udwm_dwmsetwindowattribute_cpp, dwm.dwmsetwindowattribute, dwmapi/DwmSetWindowAttribute, winui._udwm_dwmsetwindowattribute
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
req.dll: Dwmapi.dll; Uxtheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmSetWindowAttribute
 - dwmapi/DwmSetWindowAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - uxtheme.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
api_name:
 - DwmSetWindowAttribute
---

# DwmSetWindowAttribute function


## -description

Sets the value of Desktop Window Manager (DWM) non-client rendering attributes for a window. For programming guidance, and code examples, see [Controlling non-client region rendering](/windows/desktop/dwm/composition-ovw#controlling-non-client-region-rendering).

## -parameters

### -param hwnd [in]

The handle to the window for which the attribute value is to be set.

### -param dwAttribute [in]

A flag describing which value to set, specified as a value of the [DWMWINDOWATTRIBUTE](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) enumeration. This parameter specifies which attribute to set, and the *pvAttribute* parameter points to an object containing the attribute value.

### -param pvAttribute [in]

A pointer to an object containing the attribute value to set. The type of the value set depends on the value of the *dwAttribute* parameter. The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter.

### -param cbAttribute [in]

The size, in bytes, of the attribute value being set via the *pvAttribute* parameter. The type of the value set, and therefore its size in bytes, depends on the value of the *dwAttribute* parameter.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

If Desktop Composition has been disabled (Windows 7 and earlier), then this function returns **DWM_E_COMPOSITIONDISABLED**.

## -remarks

It's not valid to call this function with the *dwAttribute* parameter set to **DWMWA_NCRENDERING_ENABLED**. To enable or disable non-client rendering, you should use the **DWMWA_NCRENDERING_POLICY** attribute, and set the desired value. For more info, and a code example, see [Controlling non-client region rendering](/windows/desktop/dwm/composition-ovw#controlling-non-client-region-rendering).

## -see-also

* [DwmGetWindowAttribute function](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
* [Enable and control DWM composition](/windows/desktop/dwm/composition-ovw)

