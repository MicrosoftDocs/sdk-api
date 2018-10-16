---
UID: NS:shobjidl_core.THUMBBUTTON
title: THUMBBUTTON
author: windows-sdk-content
description: Used by methods of the ITaskbarList3 interface to define buttons used in a toolbar embedded in a window's thumbnail representation.
old-location: shell\THUMBBUTTON.htm
tech.root: shell
ms.assetid: c13657b2-5b96-45ae-b339-b06b13aca65d
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPTHUMBBUTTON, LPTHUMBBUTTON, LPTHUMBBUTTON structure pointer [Windows Shell], THUMBBUTTON, THUMBBUTTON structure [Windows Shell], _shell_THUMBBUTTON, shell.THUMBBUTTON, shobjidl_core/LPTHUMBBUTTON, shobjidl_core/THUMBBUTTON"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - THUMBBUTTON
product: Windows
targetos: Windows
req.typenames: THUMBBUTTON, *LPTHUMBBUTTON
req.redist: 
---

# THUMBBUTTON structure


## -description


Used by methods of the <a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a> interface to define buttons used in a toolbar embedded in a window's thumbnail representation.


## -struct-fields




### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/12c6a535-6a23-4b41-b4fd-4ed4e192d629">THUMBBUTTONMASK</a></b>

A combination of <a href="https://msdn.microsoft.com/12c6a535-6a23-4b41-b4fd-4ed4e192d629">THUMBBUTTONMASK</a> values that specify which members of this structure contain valid data; other members are ignored, with the exception of <b>iId</b>, which is always required.


### -field iId

Type: <b>UINT</b>

The application-defined identifier of the button, unique within the toolbar.


### -field iBitmap

Type: <b>UINT</b>

The zero-based index of the button image within the image list set through <a href="https://msdn.microsoft.com/5c288b64-8630-42ca-9821-8e131f11f76d">ITaskbarList3::ThumbBarSetImageList</a>.


### -field hIcon

Type: <b>HICON</b>

The handle of an icon to use as the button image.


### -field szTip

Type: <b>WCHAR[260]</b>

A wide character array that contains the text of the button's tooltip, displayed when the mouse pointer hovers over the button.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/601a2517-cfce-4edb-b2ca-e2ed8a365a0d">THUMBBUTTONFLAGS</a></b>

A combination of <a href="https://msdn.microsoft.com/601a2517-cfce-4edb-b2ca-e2ed8a365a0d">THUMBBUTTONFLAGS</a> values that control specific states and behaviors of the button.


## -remarks



When a button is clicked, a <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> message that contains the button ID is sent to the associated application window. The application handles whatever action it has assigned to the button.

<h3><a id="Button_Images"></a><a id="button_images"></a><a id="BUTTON_IMAGES"></a>Button Images</h3>
When using an icon, specified through the <b>hIcon</b> member, the taskbar makes its own copy of the icon. It is the caller's responsibility to free the handle it passed in <b>hIcon</b> when it is no longer needed.



If both an icon and an image list are specified for a button's image, the icon is used if possible. If for some reason the attempt to retrieve the icon fails, the image from the image list is used.

Applications must provide these button images:
            
                    <ul>
<li>The button in its default active state.</li>
<li>Images suitable for use with high-dpi (dots per inch) displays.</li>
</ul>


Images must be 32-bit and of dimensions <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>(SM_CXICON) x <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>(SM_CYICON). The toolbar itself provides visuals for a button's clicked, disabled, and hover states.




## -see-also




<a href="https://msdn.microsoft.com/5d573879-aa90-41d9-a9b7-b813dafa78ae">ITaskbarList3::ThumbBarAddButtons</a>



<a href="https://msdn.microsoft.com/5bb38b1e-dc09-4868-b424-f11beca6e64f">ITaskbarList3::ThumbBarUpdateButtons</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>



<a href="https://msdn.microsoft.com/4936FF67-19EE-4963-BE4C-3D40350C64A9">Taskbar Thumbnail Toolbar Sample</a>
 

 

