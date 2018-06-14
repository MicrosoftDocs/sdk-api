---
UID: TP:magapi
ms.assetid: 19ca8483-79f5-3a9e-a85d-cd3f31a764c4
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Magnification API

## -description

Overview of the Magnification API technology.

To develop Magnification API, you need these headers:

 * [magnification.h](../magnification/index.md)

For the programming guide, see [Magnification API](/previous-versions/windows/desktop/magapi).

## Functions

| Title   | Description   |
| ---- |:---- |
| [MagGetColorEffect function](..\magnification\nf-magnification-maggetcoloreffect.md) | Gets the color transformation matrix for a magnifier control. |
| [MagGetFullscreenColorEffect function](..\magnification\nf-magnification-maggetfullscreencoloreffect.md) | Retrieves the color transformation matrix associated with the full-screen magnifier. |
| [MagGetFullscreenTransform function](..\magnification\nf-magnification-maggetfullscreentransform.md) | Retrieves the magnification settings for the full-screen magnifier. |
| [MagGetImageScalingCallback function](..\magnification\nf-magnification-maggetimagescalingcallback.md) | Retrieves the registered callback function that implements a custom transform for image scaling. |
| [MagGetInputTransform function](..\magnification\nf-magnification-maggetinputtransform.md) | Retrieves the current input transformation for pen and touch input, represented as a source rectangle and a destination rectangle. |
| [MagGetWindowFilterList function](..\magnification\nf-magnification-maggetwindowfilterlist.md) | Retrieves the list of windows that are magnified or excluded from magnification. |
| [MagGetWindowSource function](..\magnification\nf-magnification-maggetwindowsource.md) | Gets the rectangle of the area that is being magnified. |
| [MagGetWindowTransform function](..\magnification\nf-magnification-maggetwindowtransform.md) | Retrieves the transformation matrix associated with a magnifier control. |
| [MagInitialize function](..\magnification\nf-magnification-maginitialize.md) | Creates and initializes the magnifier run-time objects. |
| [MagSetColorEffect function](..\magnification\nf-magnification-magsetcoloreffect.md) | Sets the color transformation matrix for a magnifier control. |
| [MagSetFullscreenColorEffect function](..\magnification\nf-magnification-magsetfullscreencoloreffect.md) | Changes the color transformation matrix associated with the full-screen magnifier. |
| [MagSetFullscreenTransform function](..\magnification\nf-magnification-magsetfullscreentransform.md) | Changes the magnification settings for the full-screen magnifier. |
| [MagSetImageScalingCallback function](..\magnification\nf-magnification-magsetimagescalingcallback.md) | Sets the callback function for external image filtering and scaling. |
| [MagSetInputTransform function](..\magnification\nf-magnification-magsetinputtransform.md) | Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle. |
| [MagSetWindowFilterList function](..\magnification\nf-magnification-magsetwindowfilterlist.md) | Sets the list of windows to be magnified or the list of windows to be excluded from magnification. |
| [MagSetWindowSource function](..\magnification\nf-magnification-magsetwindowsource.md) | Sets the source rectangle for the magnification window. |
| [MagSetWindowTransform function](..\magnification\nf-magnification-magsetwindowtransform.md) | Sets the transformation matrix for a magnifier control. |
| [MagShowSystemCursor function](..\magnification\nf-magnification-magshowsystemcursor.md) | Shows or hides the system cursor. |
| [MagUninitialize function](..\magnification\nf-magnification-maguninitialize.md) | Destroys the magnifier run-time objects. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [MagImageScalingCallback callback function](..\magnification\nc-magnification-magimagescalingcallback.md) | Prototype for a callback function that implements a custom transform for image scaling. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [tagMAGCOLOREFFECT structure](..\magnification\ns-magnification-tagmagcoloreffect.md) | Describes a color transformation matrix that a magnifier control uses to apply a color effect to magnified screen content. |
| [tagMAGIMAGEHEADER structure](..\magnification\ns-magnification-tagmagimageheader.md) | Describes an image format. |
| [tagMAGTRANSFORM structure](..\magnification\ns-magnification-tagmagtransform.md) | Describes a transformation matrix that a magnifier control uses to magnify screen content. |
