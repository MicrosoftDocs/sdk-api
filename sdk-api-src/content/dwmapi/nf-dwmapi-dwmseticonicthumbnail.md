---
UID: NF:dwmapi.DwmSetIconicThumbnail
title: DwmSetIconicThumbnail function (dwmapi.h)
description: Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation. The taskbar can use this bitmap as a thumbnail switch target for the window or tab.
helpviewer_keywords: ["0","DWM_SIT_DISPLAYFRAME","DwmSetIconicThumbnail","DwmSetIconicThumbnail function [Desktop Window Manager]","_udwm_dwmseticonicthumbnail","_udwm_dwmseticonicthumbnail_cpp","dwm.dwmseticonicthumbnail","dwmapi/DwmSetIconicThumbnail","winui._udwm_dwmseticonicthumbnail"]
old-location: dwm\dwmseticonicthumbnail.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmseticonicthumbnail.htm
ms.date: 12/05/2018
ms.keywords: 0, DWM_SIT_DISPLAYFRAME, DwmSetIconicThumbnail, DwmSetIconicThumbnail function [Desktop Window Manager], _udwm_dwmseticonicthumbnail, _udwm_dwmseticonicthumbnail_cpp, dwm.dwmseticonicthumbnail, dwmapi/DwmSetIconicThumbnail, winui._udwm_dwmseticonicthumbnail
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DwmSetIconicThumbnail
 - dwmapi/DwmSetIconicThumbnail
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
 - Dwmapi.dll
 - uxtheme.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
api_name:
 - DwmSetIconicThumbnail
---

# DwmSetIconicThumbnail function


## -description

Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation. The taskbar can use this bitmap as a thumbnail switch target for the window or tab.

## -parameters

### -param hwnd [in]

A handle to the window or tab. This window must belong to the calling process.

### -param hbmp [in]

A handle to the bitmap to represent the window that <i>hwnd</i> specifies.

### -param dwSITFlags [in]

The display options for the thumbnail. One of the following values:



#### 0 (0x00000000)

No frame is displayed around the provided thumbnail.



#### DWM_SIT_DISPLAYFRAME (0x00000001)

Displays a frame around the provided thumbnail.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An application typically calls the <b>DwmSetIconicThumbnail</b> function after it receives a <a href="/windows/desktop/dwm/wm-dwmsendiconicthumbnail">WM_DWMSENDICONICTHUMBNAIL</a> message for its window. The thumbnail should not exceed the maximum x-coordinate and y-coordinate that are specified in that message. The thumbnail must also have a 32-bit color depth.

The application calls <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps">DwmInvalidateIconicBitmaps</a> to indicate to the Desktop Window Manager (DWM) that the iconic thumbnail and live preview bitmaps are out-of-date and should be refreshed. The DWM then requests new versions from the window when they are needed. However, if the DWM bitmap cache is full, DWM will not request updated versions.

The DWM uses a copy of the bitmap, but the application can release this copy at any time because of memory constraints. If the copy is released, the window is not notified, but it might receive a subsequent <a href="/windows/desktop/dwm/wm-dwmsendiconicthumbnail">WM_DWMSENDICONICTHUMBNAIL</a> request when its thumbnail is needed again. The caller retains ownership of the original bitmap and is responsible for freeing the resources that it uses when it is no longer needed.


#### Examples

Before calling <b>DwmSetIconicThumbnail</b>, the application must first call the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a> function to set the <b>DWMWA_FORCE_ICONIC_REPRESENTATION</b> and <b>DWMWA_HAS_ICONIC_BITMAP</b> attributes, as shown in the following example.


```cpp
            // Set DWM window attributes to provide the iconic bitmap, and 
            // to always render the thumbnail using the iconic bitmap.
            BOOL fForceIconic = TRUE;
            BOOL fHasIconicBitmap = TRUE;

            DwmSetWindowAttribute(
                hwnd,
                DWMWA_FORCE_ICONIC_REPRESENTATION,
                &fForceIconic,
                sizeof(fForceIconic));

            DwmSetWindowAttribute(
                hwnd,
                DWMWA_HAS_ICONIC_BITMAP,
                &fHasIconicBitmap,
                sizeof(fHasIconicBitmap));

```


Next, the application calls the <b>DwmSetIconicThumbnail</b> function in response to a <a href="/windows/desktop/dwm/wm-dwmsendiconicthumbnail">WM_DWMSENDICONICTHUMBNAIL</a> message, as shown in the following example.


```cpp
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;

```


For the complete example code, see the <a href="/windows/desktop/dwm/dwm-sample-customizethumbnail">Customize an Iconic Thumbnail and a Live Preview Bitmap</a> sample.