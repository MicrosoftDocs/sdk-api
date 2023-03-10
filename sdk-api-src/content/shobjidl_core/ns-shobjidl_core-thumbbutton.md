---
UID: NS:shobjidl_core.THUMBBUTTON
title: THUMBBUTTON (shobjidl_core.h)
description: Used by methods of the ITaskbarList3 interface to define buttons used in a toolbar embedded in a window's thumbnail representation.
helpviewer_keywords: ["*LPTHUMBBUTTON","LPTHUMBBUTTON","LPTHUMBBUTTON structure pointer [Windows Shell]","THUMBBUTTON","THUMBBUTTON structure [Windows Shell]","_shell_THUMBBUTTON","shell.THUMBBUTTON","shobjidl_core/LPTHUMBBUTTON","shobjidl_core/THUMBBUTTON"]
old-location: shell\THUMBBUTTON.htm
tech.root: shell
ms.assetid: c13657b2-5b96-45ae-b339-b06b13aca65d
ms.date: 12/05/2018
ms.keywords: '*LPTHUMBBUTTON, LPTHUMBBUTTON, LPTHUMBBUTTON structure pointer [Windows Shell], THUMBBUTTON, THUMBBUTTON structure [Windows Shell], _shell_THUMBBUTTON, shell.THUMBBUTTON, shobjidl_core/LPTHUMBBUTTON, shobjidl_core/THUMBBUTTON'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: THUMBBUTTON, *LPTHUMBBUTTON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - THUMBBUTTON
 - shobjidl_core/THUMBBUTTON
 - LPTHUMBBUTTON
 - shobjidl_core/LPTHUMBBUTTON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - THUMBBUTTON
---

# THUMBBUTTON structure


## -description

Used by methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a> interface to define buttons used in a toolbar embedded in a window's thumbnail representation.

## -struct-fields

### -field dwMask

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask">THUMBBUTTONMASK</a></b>

A combination of <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask">THUMBBUTTONMASK</a> values that specify which members of this structure contain valid data; other members are ignored, with the exception of <b>iId</b>, which is always required.

### -field iId

Type: <b>UINT</b>

The application-defined identifier of the button, unique within the toolbar.

### -field iBitmap

Type: <b>UINT</b>

The zero-based index of the button image within the image list set through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist">ITaskbarList3::ThumbBarSetImageList</a>.

### -field hIcon

Type: <b>HICON</b>

The handle of an icon to use as the button image.

### -field szTip

Type: <b>WCHAR[260]</b>

A wide character array that contains the text of the button's tooltip, displayed when the mouse pointer hovers over the button.

### -field dwFlags

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags">THUMBBUTTONFLAGS</a></b>

A combination of <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags">THUMBBUTTONFLAGS</a> values that control specific states and behaviors of the button.

## -remarks

When a button is clicked, a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message that contains the button ID is sent to the associated application window. The application handles whatever action it has assigned to the button.

<h3><a id="Button_Images"></a><a id="button_images"></a><a id="BUTTON_IMAGES"></a>Button Images</h3>
When using an icon, specified through the <b>hIcon</b> member, the taskbar makes its own copy of the icon. It is the caller's responsibility to free the handle it passed in <b>hIcon</b> when it is no longer needed.



If both an icon and an image list are specified for a button's image, the icon is used if possible. If for some reason the attempt to retrieve the icon fails, the image from the image list is used.

Applications must provide these button images:
            
<ul>
<li>The button in its default active state.</li>
<li>Images suitable for use with high-dpi (dots per inch) displays.</li>
</ul>


Images must be 32-bit and of dimensions <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>(SM_CXICON) x <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>(SM_CYICON). The toolbar itself provides visuals for a button's clicked, disabled, and hover states.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons">ITaskbarList3::ThumbBarAddButtons</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons">ITaskbarList3::ThumbBarUpdateButtons</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>



<a href="/previous-versions/windows/desktop/legacy/ee663597(v=vs.85)">Taskbar Thumbnail Toolbar Sample</a>