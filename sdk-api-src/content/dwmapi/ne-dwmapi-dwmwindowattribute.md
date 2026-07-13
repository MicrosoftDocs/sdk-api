---
UID: NE:dwmapi.DWMWINDOWATTRIBUTE
title: DWMWINDOWATTRIBUTE (dwmapi.h)
description: Flags used by the [DwmGetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) and [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) functions.
helpviewer_keywords: ["DWMWA_ALLOW_NCPAINT","DWMWA_CAPTION_BUTTON_BOUNDS","DWMWA_CLOAK","DWMWA_CLOAKED","DWMWA_DISALLOW_PEEK","DWMWA_EXCLUDED_FROM_PEEK","DWMWA_EXTENDED_FRAME_BOUNDS","DWMWA_FLIP3D_POLICY","DWMWA_FORCE_ICONIC_REPRESENTATION","DWMWA_FREEZE_REPRESENTATION","DWMWA_HAS_ICONIC_BITMAP","DWMWA_LAST","DWMWA_NCRENDERING_ENABLED","DWMWA_NCRENDERING_POLICY","DWMWA_NONCLIENT_RTL_LAYOUT","DWMWA_TRANSITIONS_FORCEDISABLED","DWMWINDOWATTRIBUTE","DWMWINDOWATTRIBUTE enumeration [Desktop Window Manager]","_udwm_dwmwindowattribute","_udwm_dwmwindowattribute_cpp","dwm.dwmwindowattribute","dwmapi/DWMWA_ALLOW_NCPAINT","dwmapi/DWMWA_CAPTION_BUTTON_BOUNDS","dwmapi/DWMWA_CLOAK","dwmapi/DWMWA_CLOAKED","dwmapi/DWMWA_DISALLOW_PEEK","dwmapi/DWMWA_EXCLUDED_FROM_PEEK","dwmapi/DWMWA_EXTENDED_FRAME_BOUNDS","dwmapi/DWMWA_FLIP3D_POLICY","dwmapi/DWMWA_FORCE_ICONIC_REPRESENTATION","dwmapi/DWMWA_FREEZE_REPRESENTATION","dwmapi/DWMWA_HAS_ICONIC_BITMAP","dwmapi/DWMWA_LAST","dwmapi/DWMWA_NCRENDERING_ENABLED","dwmapi/DWMWA_NCRENDERING_POLICY","dwmapi/DWMWA_NONCLIENT_RTL_LAYOUT","dwmapi/DWMWA_TRANSITIONS_FORCEDISABLED","dwmapi/DWMWINDOWATTRIBUTE","winui._udwm_dwmwindowattribute", "DWMWA_USE_IMMERSIVE_DARK_MODE", "DWMWA_WINDOW_CORNER_PREFERENCE", "DWMWA_BORDER_COLOR", "DWMWA_CAPTION_COLOR", "DWMWA_TEXT_COLOR", "DWMWA_VISIBLE_FRAME_BORDER_THICKNESS"]
old-location: dwm\dwmwindowattribute.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\enums\dwmwindowattribute.htm
ms.date: 01/21/2024
ms.keywords: DWMWA_ALLOW_NCPAINT, DWMWA_CAPTION_BUTTON_BOUNDS, DWMWA_CLOAK, DWMWA_CLOAKED, DWMWA_DISALLOW_PEEK, DWMWA_EXCLUDED_FROM_PEEK, DWMWA_EXTENDED_FRAME_BOUNDS, DWMWA_FLIP3D_POLICY, DWMWA_FORCE_ICONIC_REPRESENTATION, DWMWA_FREEZE_REPRESENTATION, DWMWA_HAS_ICONIC_BITMAP, DWMWA_LAST, DWMWA_NCRENDERING_ENABLED, DWMWA_NCRENDERING_POLICY, DWMWA_NONCLIENT_RTL_LAYOUT, DWMWA_TRANSITIONS_FORCEDISABLED, DWMWINDOWATTRIBUTE, DWMWINDOWATTRIBUTE enumeration [Desktop Window Manager], _udwm_dwmwindowattribute, _udwm_dwmwindowattribute_cpp, dwm.dwmwindowattribute, dwmapi/DWMWA_ALLOW_NCPAINT, dwmapi/DWMWA_CAPTION_BUTTON_BOUNDS, dwmapi/DWMWA_CLOAK, dwmapi/DWMWA_CLOAKED, dwmapi/DWMWA_DISALLOW_PEEK, dwmapi/DWMWA_EXCLUDED_FROM_PEEK, dwmapi/DWMWA_EXTENDED_FRAME_BOUNDS, dwmapi/DWMWA_FLIP3D_POLICY, dwmapi/DWMWA_FORCE_ICONIC_REPRESENTATION, dwmapi/DWMWA_FREEZE_REPRESENTATION, dwmapi/DWMWA_HAS_ICONIC_BITMAP, dwmapi/DWMWA_LAST, dwmapi/DWMWA_NCRENDERING_ENABLED, dwmapi/DWMWA_NCRENDERING_POLICY, dwmapi/DWMWA_NONCLIENT_RTL_LAYOUT, dwmapi/DWMWA_TRANSITIONS_FORCEDISABLED, dwmapi/DWMWINDOWATTRIBUTE, winui._udwm_dwmwindowattribute
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWMWINDOWATTRIBUTE
 - dwmapi/DWMWINDOWATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - DWMWINDOWATTRIBUTE
prerelease: false
---

## -description

Options used by the [DwmGetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) and [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) functions.

## -enum-fields

### -field DWMWA_NCRENDERING_ENABLED

**IMPORTANT**. The value of **DWMWA_NCRENDERING_ENABLED** is 1.

<pre><code class="lang-syntax">
typedef enum DWMWINDOWATTRIBUTE {
  DWMWA_NCRENDERING_ENABLED = 1,
  DWMWA_NCRENDERING_POLICY,
  ...
</code></pre>

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute">DwmGetWindowAttribute</a>. Discovers whether non-client rendering is enabled. The retrieved value is of type <b>BOOL</b>. <b>TRUE</b> if non-client rendering is enabled; otherwise, <b>FALSE</b>.

### -field DWMWA_NCRENDERING_POLICY

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Sets the non-client rendering policy. The <i>pvAttribute</i> parameter points to a value from the <a href="/windows/win32/api/dwmapi/ne-dwmapi-dwmncrenderingpolicy">DWMNCRENDERINGPOLICY</a> enumeration.

### -field DWMWA_TRANSITIONS_FORCEDISABLED

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Enables or forcibly disables DWM transitions. The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> to disable transitions, or <b>FALSE</b> to enable transitions.

### -field DWMWA_ALLOW_NCPAINT

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Enables content rendered in the non-client area to be visible on the frame drawn by DWM. The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> to enable content rendered in the non-client area to be visible on the frame; otherwise, <b>FALSE</b>.

### -field DWMWA_CAPTION_BUTTON_BOUNDS

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute">DwmGetWindowAttribute</a>. Retrieves the bounds of the caption button area in the window-relative space. The retrieved value is of type <a href="/windows/win32/api/windef/ns-windef-rect">RECT</a>. If the window is minimized or otherwise not visible to the user, then the value of the **RECT** retrieved is undefined. You should check whether the retrieved **RECT** contains a boundary that you can work with, and if it doesn't then you can conclude that the window is minimized or otherwise not visible.

### -field DWMWA_NONCLIENT_RTL_LAYOUT

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Specifies whether non-client content is right-to-left (RTL) mirrored. The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> if the non-client content is right-to-left (RTL) mirrored; otherwise, <b>FALSE</b>.

### -field DWMWA_FORCE_ICONIC_REPRESENTATION

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Forces the window to display an iconic thumbnail or peek representation (a static bitmap), even if a live or snapshot representation of the window is available. This value is normally set during a window's creation, and not changed throughout the window's lifetime. Some scenarios, however, might require the value to change over time. The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> to require a iconic thumbnail or peek representation; otherwise, <b>FALSE</b>.

### -field DWMWA_FLIP3D_POLICY

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Sets how Flip3D treats the window. The <i>pvAttribute</i> parameter points to a value from the <a href="/windows/win32/api/dwmapi/ne-dwmapi-dwmflip3dwindowpolicy">DWMFLIP3DWINDOWPOLICY</a> enumeration.

### -field DWMWA_EXTENDED_FRAME_BOUNDS

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute">DwmGetWindowAttribute</a>. Retrieves the extended frame bounds rectangle in screen space. The retrieved value is of type <a href="/windows/win32/api/windef/ns-windef-rect">RECT</a>.

### -field DWMWA_HAS_ICONIC_BITMAP

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. The window will provide a bitmap for use by DWM as an iconic thumbnail or peek representation (a static bitmap) for the window. <b>DWMWA_HAS_ICONIC_BITMAP</b> can be specified with <b>DWMWA_FORCE_ICONIC_REPRESENTATION</b>. <b>DWMWA_HAS_ICONIC_BITMAP</b> normally is set during a window's creation and not changed throughout the window's lifetime. Some scenarios, however, might require the value to change over time. The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>.  <b>TRUE</b> to inform DWM that the window will provide an iconic thumbnail or peek representation; otherwise, <b>FALSE</b>.

<b>Windows Vista and earlier: </b>This value is not supported.

### -field DWMWA_DISALLOW_PEEK

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Do not show peek preview for the window. The peek view shows a full-sized preview of the window when the mouse hovers over the window's thumbnail in the taskbar. If this attribute is set, hovering the mouse pointer over the window's thumbnail dismisses peek (in case another window in the group has a peek preview showing). The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> to prevent peek functionality, or <b>FALSE</b> to allow it.

<b>Windows Vista and earlier: </b>This value is not supported.

### -field DWMWA_EXCLUDED_FROM_PEEK

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Prevents a window from fading to a glass sheet when peek is invoked. The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> to prevent the window from fading during another window's peek, or <b>FALSE</b> for normal behavior.

<b>Windows Vista and earlier: </b>This value is not supported.

### -field DWMWA_CLOAK

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Cloaks the window such that it is not visible to the user. The window is still composed by DWM.

<b>Using with DirectComposition: </b>Use the DWMWA_CLOAK flag to cloak the layered child window when animating a representation of the window's content via a DirectComposition visual that has been associated with the layered child window. For more details on this usage case, see <a href="/windows/desktop/directcomp/how-to--animate-the-bitmap-of-a-layered-child-window">How to animate the bitmap of a layered child window</a>.

<b>Windows 7 and earlier: </b>This value is not supported.

### -field DWMWA_CLOAKED

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute">DwmGetWindowAttribute</a>. If the window is cloaked, provides one of the following values explaining why.

<b>DWM_CLOAKED_APP</b> (value 0x00000001). The window was cloaked by its owner application.

<b>DWM_CLOAKED_SHELL</b> (value 0x00000002). The window was cloaked by the Shell.

<b>DWM_CLOAKED_INHERITED</b> (value 0x00000004). The cloak value was inherited from its owner window.

<b>Windows 7 and earlier: </b>This value is not supported.

### -field DWMWA_FREEZE_REPRESENTATION

Use with <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a>. Freeze the window's thumbnail image with its current visuals. Do no further live updates on the thumbnail image to match the window's contents.

<b>Windows 7 and earlier: </b>This value is not supported.

### -field DWMWA_USE_HOSTBACKDROPBRUSH

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Enables a non-UWP window to use host backdrop brushes. If this flag is set, then a Win32 app that calls [Windows::UI::Composition](/uwp/api/windows.ui.composition) APIs can build transparency effects using the host backdrop brush (see [Compositor.CreateHostBackdropBrush](/uwp/api/windows.ui.composition.compositor.createhostbackdropbrush)). The <i>pvAttribute</i> parameter points to a value of type <b>BOOL</b>. <b>TRUE</b> to enable host backdrop brushes for the window, or <b>FALSE</b> to disable it.

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_USE_IMMERSIVE_DARK_MODE : 20

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Allows the window frame for this window to be drawn in dark mode colors when the dark mode system setting is enabled. For compatibility reasons, all windows default to light mode regardless of the system setting. The <i>pvAttribute</i> parameter points to a value of type **BOOL**. <b>TRUE</b> to honor dark mode for the window, <b>FALSE</b> to always use light mode.

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_WINDOW_CORNER_PREFERENCE : 33

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Specifies the rounded corner preference for a window. The <i>pvAttribute</i> parameter points to a value of type [DWM_WINDOW_CORNER_PREFERENCE](ne-dwmapi-dwm_window_corner_preference.md).

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_BORDER_COLOR

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Specifies the color of the window border. The <i>pvAttribute</i> parameter points to a value of type [COLORREF](/windows/win32/gdi/colorref). The app is responsible for changing the border color according to state changes, such as a change in window activation. 

Specifying **DWMWA_COLOR_NONE** (value 0xFFFFFFFE) for the color will suppress the drawing of the window border.  This makes it possible to have a rounded window with no border.

Specifying **DWMWA_COLOR_DEFAULT** (value 0xFFFFFFFF) for the color will reset the window back to using the system's default behavior for the border color.

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_CAPTION_COLOR

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Specifies the color of the caption. The <i>pvAttribute</i> parameter points to a value of type [COLORREF](/windows/win32/gdi/colorref). 

Specifying **DWMWA_COLOR_DEFAULT** (value 0xFFFFFFFF) for the color will reset the window back to using the system's default behavior for the caption color.

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_TEXT_COLOR

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Specifies the color of the caption text. The <i>pvAttribute</i> parameter points to a value of type [COLORREF](/windows/win32/gdi/colorref). 

Specifying **DWMWA_COLOR_DEFAULT** (value 0xFFFFFFFF) for the color will reset the window back to using the system's default behavior for the caption text color.

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_VISIBLE_FRAME_BORDER_THICKNESS

Use with [DwmGetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute). Retrieves the width of the outer border that the DWM would draw around this window. The value can vary depending on the DPI of the window. The <i>pvAttribute</i> parameter points to a value of type **UINT**. 

This value is supported starting with Windows 11 Build 22000.

### -field DWMWA_SYSTEMBACKDROP_TYPE

Use with [DwmGetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) or [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute). Retrieves or specifies the system-drawn backdrop material of a window, including behind the non-client area. The *pvAttribute* parameter points to a value of type [DWM_SYSTEMBACKDROP_TYPE](ne-dwmapi-dwm_systembackdrop_type.md). 

This value is supported starting with Windows 11 Build 22621.


### -field DWMWA_REDIRECTIONBITMAP_ALPHA

Use with
[DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
. Enables or disables the use of the alpha channel in the window's redirection
bitmap. If this attribute is set to true, the window must contain premultiplied
alpha values in each pixel. If it is false, the alpha is ignored and the
redirection bitmap is treated as fully opaque. This attribute defaults to false.

This value is supported starting with Windows 11 Build 26100.

### -field DWMWA_BORDER_MARGINS

Use with [DwmSetWindowAttribute](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
. Specifies the override location of the window border, as a distance from each
edge. The *pvAttribute* parameter points to a value of type FRAME_MARGIN.

A value of all zeros disables the override set by this attribute, resulting in
default window borders. Otherwise, all values must be greater than or equal to 1.

Each value in the FRAME_MARGIN (left, right, top, bottom) indicates a distance
inwards from each edge of the window. Non-zero border margins forces the window
to have a border and sets the location of the border. Window contents covered
by or outside the border are clipped.

This value will be supported in an upcoming update to Windows 11 build 26100.

### -field DWMWA_LAST

The maximum recognized <b>DWMWINDOWATTRIBUTE</b> value, used for validation purposes.

## -see-also

* [DwmGetWindowAttribute function](/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
* [DwmSetWindowAttribute function](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
* [Enable and control DWM composition](/windows/desktop/dwm/composition-ovw)
