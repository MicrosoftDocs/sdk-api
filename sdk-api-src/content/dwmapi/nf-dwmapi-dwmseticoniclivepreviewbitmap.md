---
UID: NF:dwmapi.DwmSetIconicLivePreviewBitmap
title: DwmSetIconicLivePreviewBitmap function (dwmapi.h)
description: Sets a static, iconic bitmap to display a live preview (also known as a Peek preview) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.
helpviewer_keywords: ["DWM_SIT_DISPLAYFRAME","DwmSetIconicLivePreviewBitmap","DwmSetIconicLivePreviewBitmap function [Desktop Window Manager]","_udwm_dwmseticoniclivepreviewbitmap","_udwm_dwmseticoniclivepreviewbitmap_cpp","dwm.dwmseticoniclivepreviewbitmap","dwmapi/DwmSetIconicLivePreviewBitmap","winui._udwm_dwmseticoniclivepreviewbitmap"]
old-location: dwm\dwmseticoniclivepreviewbitmap.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmseticoniclivepreviewbitmap.htm
ms.date: 12/05/2018
ms.keywords: DWM_SIT_DISPLAYFRAME, DwmSetIconicLivePreviewBitmap, DwmSetIconicLivePreviewBitmap function [Desktop Window Manager], _udwm_dwmseticoniclivepreviewbitmap, _udwm_dwmseticoniclivepreviewbitmap_cpp, dwm.dwmseticoniclivepreviewbitmap, dwmapi/DwmSetIconicLivePreviewBitmap, winui._udwm_dwmseticoniclivepreviewbitmap
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
 - DwmSetIconicLivePreviewBitmap
 - dwmapi/DwmSetIconicLivePreviewBitmap
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
 - DwmSetIconicLivePreviewBitmap
---

# DwmSetIconicLivePreviewBitmap function


## -description

Sets a static, iconic bitmap to display a <i>live preview</i> (also known as a <i>Peek preview</i>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.

## -parameters

### -param hwnd [in]

A handle to the window. This window must belong to the calling process.

### -param hbmp [in]

A handle to the bitmap to represent the window that <i>hwnd</i> specifies.

### -param pptClient [in, optional]

The offset of a tab window's <i>client region</i> (the content area inside the client window frame) from the host window's frame. This offset enables the tab window's contents to be drawn correctly in a live preview  when it is drawn without its frame.

### -param dwSITFlags [in]

The display options for the live preview. This parameter can be 0 or the following value.

#### DWM_SIT_DISPLAYFRAME (0x00000001)

0x00000001. Displays a frame around the provided bitmap.

## -returns

Returns <b>S_OK</b> if the function succeeds, or an error value otherwise. Note that because this bitmap is not cached, if the window is not being previewed when an application calls this function, the function returns a success code but the bitmap is discarded and not used.

## -remarks

A <i>live preview</i> (also known as a <i>Peek preview</i>) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window. This view is a full-sized view of the window and can be a snapshot or an iconic representation.

A window typically calls the <b>DwmSetIconicLivePreviewBitmap</b> function in response to a <a href="/windows/desktop/dwm/wm-dwmsendiconiclivepreviewbitmap">WM_DWMSENDICONICLIVEPREVIEWBITMAP</a> message. The returned bitmap must not be larger than the client area of the window or frame and must have 32-bit color depth.

The Desktop Window Manager (DWM) uses a copy of the bitmap, but the caller retains ownership of the original bitmap and is responsible for freeing the resources that it uses when it is no longer needed. The DWM does not keep its copy of the bitmap when the DWM stops displaying the live preview representation.


#### Examples

 To set a static, iconic bitmap to use as a live preview for the application's window, an application calls the <b>DwmSetIconicLivePreviewBitmap</b> function. To set this bitmap, the application must call <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a> to set window attributes for non-client rendering to  <b>DWMWA_FORCE_ICONIC_REPRESENTATION</b> and <b>DWMWA_HAS_ICONIC_BITMAP</b>,  as shown in the following code. 


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


Then, the application calls <b>DwmSetIconicLivePreviewBitmap</b>  to respond to the <a href="/windows/desktop/dwm/wm-dwmsendiconiclivepreviewbitmap">WM_DWMSENDICONICLIVEPREVIEWBITMAP</a> message, as shown in the following code.


```cpp
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;

```


For the complete example, see the  <a href="/windows/desktop/dwm/dwm-sample-customizethumbnail">Customize an Iconic Thumbnail and a Live Preview Bitmap</a> sample.