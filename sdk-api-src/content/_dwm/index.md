---
UID: TP:dwm
ms.assetid: ffe04284-f2a5-3f9e-9fca-a858703230a8
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Desktop Window Manager (DWM)



Overview of the Desktop Window Manager (DWM) technology.

To develop Desktop Window Manager (DWM), you need these headers:

 * [dwmapi.h](..\dwmapi\index.md)

For the programming guide, see [Desktop Window Manager (DWM)](/windows/desktop/dwm).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DwmAttachMilContent function](..\dwmapi\nf-dwmapi-dwmattachmilcontent.md) | This function is not implemented. |
| [DwmDefWindowProc function](..\dwmapi\nf-dwmapi-dwmdefwindowproc.md) | Default window procedure for Desktop Window Manager (DWM) hit testing within the non-client area. |
| [DwmDetachMilContent function](..\dwmapi\nf-dwmapi-dwmdetachmilcontent.md) | This function is not implemented. |
| [DwmEnableBlurBehindWindow function](..\dwmapi\nf-dwmapi-dwmenableblurbehindwindow.md) | Enables the blur effect on a specified window. |
| [DwmEnableComposition function](..\dwmapi\nf-dwmapi-dwmenablecomposition.md) | Enables or disables Desktop Window Manager (DWM) composition. |
| [DwmEnableMMCSS function](..\dwmapi\nf-dwmapi-dwmenablemmcss.md) | Notifies the Desktop Window Manager (DWM) to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive. |
| [DwmExtendFrameIntoClientArea function](..\dwmapi\nf-dwmapi-dwmextendframeintoclientarea.md) | Extends the window frame into the client area. |
| [DwmFlush function](..\dwmapi\nf-dwmapi-dwmflush.md) | Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made. This compensates for very complex scenes or calling processes with very low priority. |
| [DwmGetColorizationColor function](..\dwmapi\nf-dwmapi-dwmgetcolorizationcolor.md) | Retrieves the current color used for Desktop Window Manager (DWM) glass composition. |
| [DwmGetCompositionTimingInfo function](..\dwmapi\nf-dwmapi-dwmgetcompositiontiminginfo.md) | Retrieves the current composition timing information for a specified window. |
| [DwmGetGraphicsStreamClient function](..\dwmapi\nf-dwmapi-dwmgetgraphicsstreamclient.md) | This function is not implemented. |
| [DwmGetGraphicsStreamTransformHint function](..\dwmapi\nf-dwmapi-dwmgetgraphicsstreamtransformhint.md) | This function is not implemented. |
| [DwmGetTransportAttributes function](..\dwmapi\nf-dwmapi-dwmgettransportattributes.md) | Retrieves transport attributes. |
| [DwmGetUnmetTabRequirements function](..\dwmapi\nf-dwmapi-dwmgetunmettabrequirements.md) | Note  This function is publically available, but nonfunctional, for Windows 10, version 1803.Checks the requirements needed to get tabs in the application title bar for the specified window. |
| [DwmGetWindowAttribute function](..\dwmapi\nf-dwmapi-dwmgetwindowattribute.md) | Retrieves the current value of a specified attribute applied to a window. |
| [DwmInvalidateIconicBitmaps function](..\dwmapi\nf-dwmapi-dwminvalidateiconicbitmaps.md) | Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed. |
| [DwmIsCompositionEnabled function](..\dwmapi\nf-dwmapi-dwmiscompositionenabled.md) | Obtains a value that indicates whether Desktop Window Manager (DWM) composition is enabled. Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the WM_DWMCOMPOSITIONCHANGED notification. |
| [DwmModifyPreviousDxFrameDuration function](..\dwmapi\nf-dwmapi-dwmmodifypreviousdxframeduration.md) | Changes the number of monitor refreshes through which the previous frame will be displayed. DwmModifyPreviousDxFrameDuration is no longer supported. Starting with Windows 8.1, calls to DwmModifyPreviousDxFrameDuration always return E_NOTIMPL. |
| [DwmQueryThumbnailSourceSize function](..\dwmapi\nf-dwmapi-dwmquerythumbnailsourcesize.md) | Retrieves the source size of the Desktop Window Manager (DWM) thumbnail. |
| [DwmRegisterThumbnail function](..\dwmapi\nf-dwmapi-dwmregisterthumbnail.md) | Creates a Desktop Window Manager (DWM) thumbnail relationship between the destination and source windows. |
| [DwmRenderGesture function](..\dwmapi\nf-dwmapi-dwmrendergesture.md) | Notifies Desktop Window Manager (DWM) that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture. |
| [DwmSetDxFrameDuration function](..\dwmapi\nf-dwmapi-dwmsetdxframeduration.md) | Sets the number of monitor refreshes through which to display the presented frame. DwmSetDxFrameDuration is no longer supported. Starting with Windows 8.1, calls to DwmSetDxFrameDuration always return E_NOTIMPL. |
| [DwmSetIconicLivePreviewBitmap function](..\dwmapi\nf-dwmapi-dwmseticoniclivepreviewbitmap.md) | Sets a static, iconic bitmap to display a live preview (also known as a Peek preview) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab. |
| [DwmSetIconicThumbnail function](..\dwmapi\nf-dwmapi-dwmseticonicthumbnail.md) | Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation. The taskbar can use this bitmap as a thumbnail switch target for the window or tab. |
| [DwmSetPresentParameters function](..\dwmapi\nf-dwmapi-dwmsetpresentparameters.md) | Sets the present parameters for frame composition. DwmSetPresentParameters is no longer supported. Starting with Windows 8.1, calls to DwmSetPresentParameters always return E_NOTIMPL. |
| [DwmSetWindowAttribute function](..\dwmapi\nf-dwmapi-dwmsetwindowattribute.md) | Sets the value of non-client rendering attributes for a window. |
| [DwmShowContact function](..\dwmapi\nf-dwmapi-dwmshowcontact.md) | Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact. |
| [DwmTetherContact function](..\dwmapi\nf-dwmapi-dwmtethercontact.md) | Enables the graphical feedback of touch and drag interactions to the user. |
| [DwmTransitionOwnedWindow function](..\dwmapi\nf-dwmapi-dwmtransitionownedwindow.md) | Coordinates the animations of tool windows with the Desktop Window Manager (DWM). |
| [DwmUnregisterThumbnail function](..\dwmapi\nf-dwmapi-dwmunregisterthumbnail.md) | Removes a Desktop Window Manager (DWM) thumbnail relationship created by the DwmRegisterThumbnail function. |
| [DwmUpdateThumbnailProperties function](..\dwmapi\nf-dwmapi-dwmupdatethumbnailproperties.md) | Updates the properties for a Desktop Window Manager (DWM) thumbnail. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_DWM_BLURBEHIND structure](..\dwmapi\ns-dwmapi-_dwm_blurbehind.md) | Specifies Desktop Window Manager (DWM) blur-behind properties. Used by the DwmEnableBlurBehindWindow function. |
| [_DWM_PRESENT_PARAMETERS structure](..\dwmapi\ns-dwmapi-_dwm_present_parameters.md) | Specifies Desktop Window Manager (DWM) video frame parameters for frame composition. Used by the DwmSetPresentParameters function. |
| [_DWM_THUMBNAIL_PROPERTIES structure](..\dwmapi\ns-dwmapi-_dwm_thumbnail_properties.md) | Specifies Desktop Window Manager (DWM) thumbnail properties. Used by the DwmUpdateThumbnailProperties function. |
| [_DWM_TIMING_INFO structure](..\dwmapi\ns-dwmapi-_dwm_timing_info.md) | Specifies Desktop Window Manager (DWM) composition timing information. Used by the DwmGetCompositionTimingInfo function. |
| [_MilMatrix3x2D structure](..\dwmapi\ns-dwmapi-_milmatrix3x2d.md) | Specifies a 3x2 matrix that describes a transform. |
| [_UNSIGNED_RATIO structure](..\dwmapi\ns-dwmapi-_unsigned_ratio.md) | Defines a data type used by the Desktop Window Manager (DWM) APIs. It represents a generic ratio and is used for different purposes and units even within a single API. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [DWMFLIP3DWINDOWPOLICY enumeration](..\dwmapi\ne-dwmapi-dwmflip3dwindowpolicy.md) | Flags used by the DwmSetWindowAttribute function to specify the Flip3D window policy. |
| [DWMNCRENDERINGPOLICY enumeration](..\dwmapi\ne-dwmapi-dwmncrenderingpolicy.md) | Flags used by the DwmSetWindowAttribute function to specify the non-client area rendering policy. |
| [DWMTRANSITION_OWNEDWINDOW_TARGET enumeration](..\dwmapi\ne-dwmapi-dwmtransition_ownedwindow_target.md) | Identifies the target. |
| [DWMWINDOWATTRIBUTE enumeration](..\dwmapi\ne-dwmapi-dwmwindowattribute.md) | Flags used by the DwmGetWindowAttribute and DwmSetWindowAttribute functions to specify window attributes for non-client rendering. |
| [DWM_SOURCE_FRAME_SAMPLING enumeration](..\dwmapi\ne-dwmapi-dwm_source_frame_sampling.md) | Flags used by the DwmSetPresentParameters function to specify the frame sampling type. |
| [DWM_TAB_WINDOW_REQUIREMENTS enumeration](..\dwmapi\ne-dwmapi-dwm_tab_window_requirements.md) | Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar. |
| [GESTURE_TYPE enumeration](..\dwmapi\ne-dwmapi-gesture_type.md) | Identifies the gesture type specified in DwmRenderGesture. |
