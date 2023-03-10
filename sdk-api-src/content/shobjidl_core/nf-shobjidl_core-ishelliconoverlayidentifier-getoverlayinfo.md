---
UID: NF:shobjidl_core.IShellIconOverlayIdentifier.GetOverlayInfo
title: IShellIconOverlayIdentifier::GetOverlayInfo (shobjidl_core.h)
description: Provides the location of the icon overlay's bitmap.
helpviewer_keywords: ["GetOverlayInfo","GetOverlayInfo method [Windows Shell]","GetOverlayInfo method [Windows Shell]","IShellIconOverlayIdentifier interface","ISIOI_ICONFILE","ISIOI_ICONINDEX","IShellIconOverlayIdentifier interface [Windows Shell]","GetOverlayInfo method","IShellIconOverlayIdentifier.GetOverlayInfo","IShellIconOverlayIdentifier::GetOverlayInfo","_win32_IShellIconOverlayIdentifier_GetOverlayInfo","shell.IShellIconOverlayIdentifier_GetOverlayInfo","shobjidl_core/IShellIconOverlayIdentifier::GetOverlayInfo"]
old-location: shell\IShellIconOverlayIdentifier_GetOverlayInfo.htm
tech.root: shell
ms.assetid: 301dc569-738f-454f-9063-223ea6632e55
ms.date: 12/05/2018
ms.keywords: GetOverlayInfo, GetOverlayInfo method [Windows Shell], GetOverlayInfo method [Windows Shell],IShellIconOverlayIdentifier interface, ISIOI_ICONFILE, ISIOI_ICONINDEX, IShellIconOverlayIdentifier interface [Windows Shell],GetOverlayInfo method, IShellIconOverlayIdentifier.GetOverlayInfo, IShellIconOverlayIdentifier::GetOverlayInfo, _win32_IShellIconOverlayIdentifier_GetOverlayInfo, shell.IShellIconOverlayIdentifier_GetOverlayInfo, shobjidl_core/IShellIconOverlayIdentifier::GetOverlayInfo
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellIconOverlayIdentifier::GetOverlayInfo
 - shobjidl_core/IShellIconOverlayIdentifier::GetOverlayInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayIdentifier.GetOverlayInfo
---

# IShellIconOverlayIdentifier::GetOverlayInfo


## -description

Provides the location of the icon overlay's bitmap.

## -parameters

### -param pwszIconFile [out]

Type: <b>PWSTR</b>

A null-terminated Unicode string that contains the fully qualified path of the file containing the icon. The .dll, .exe, and .ico file types are all acceptable. You must set the <b>ISIOI_ICONFILE</b> flag in <i>pdwFlags</i> if you return a file name.

### -param cchMax

Type: <b>int</b>

The size of the <i>pwszIconFile</i> buffer, in Unicode characters.

### -param pIndex [out]

Type: <b>int*</b>

Pointer to an index value used to identify the icon in a file that contains multiple icons. You must set the <b>ISIOI_ICONINDEX</b> flag in <i>pdwFlags</i> if you return an index.

### -param pdwFlags [out]

Type: <b>DWORD*</b>

Pointer to a bitmap that specifies the information that is being returned by the method. This parameter can be one or both of the following values.



#### ISIOI_ICONFILE (0x00000001)

The path of the icon file is returned through <i>pwszIconFile</i>.



#### ISIOI_ICONINDEX (0x00000002)

There is more than one icon in <i>pwszIconFile</i>. The icon's index is returned through <i>pIndex</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by the Shell at startup so that the handler's icon overlay can be added to the system image list. After initialization is complete, the Shell calls <b>GetOverlayInfo</b> when it needs to display the handler's icon overlay.

<div class="alert"><b>Note</b>  Once the image has been loaded into the system image list during initialization, it cannot be changed. After initialization, the file name and index are used only to identify the icon overlay. The system will not load a new icon overlay. When <b>GetOverlayInfo</b> is called, your handler must return the same file name and index that were specified when the function was first called.</div>
<div> </div>

