---
UID: NF:shlobj_core.IShellIconOverlayManager.GetFileOverlayInfo
title: IShellIconOverlayManager::GetFileOverlayInfo (shlobj_core.h)
description: Gets the index of the icon overlay or the icon image for the specified file with the specified attributes.
helpviewer_keywords: ["GetFileOverlayInfo","GetFileOverlayInfo method [Windows Shell]","GetFileOverlayInfo method [Windows Shell]","IShellIconOverlayManager interface","IShellIconOverlayManager interface [Windows Shell]","GetFileOverlayInfo method","IShellIconOverlayManager.GetFileOverlayInfo","IShellIconOverlayManager::GetFileOverlayInfo","_win32_IShellIconOverlayManager_GetFileOverlayInfo","shell.IShellIconOverlayManager_GetFileOverlayInfo","shlobj_core/IShellIconOverlayManager::GetFileOverlayInfo"]
old-location: shell\IShellIconOverlayManager_GetFileOverlayInfo.htm
tech.root: shell
ms.assetid: 0dd918a4-64c7-4d7a-846c-0751e23c05a2
ms.date: 12/05/2018
ms.keywords: GetFileOverlayInfo, GetFileOverlayInfo method [Windows Shell], GetFileOverlayInfo method [Windows Shell],IShellIconOverlayManager interface, IShellIconOverlayManager interface [Windows Shell],GetFileOverlayInfo method, IShellIconOverlayManager.GetFileOverlayInfo, IShellIconOverlayManager::GetFileOverlayInfo, _win32_IShellIconOverlayManager_GetFileOverlayInfo, shell.IShellIconOverlayManager_GetFileOverlayInfo, shlobj_core/IShellIconOverlayManager::GetFileOverlayInfo
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IShellIconOverlayManager::GetFileOverlayInfo
 - shlobj_core/IShellIconOverlayManager::GetFileOverlayInfo
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
 - IShellIconOverlayManager.GetFileOverlayInfo
---

# IShellIconOverlayManager::GetFileOverlayInfo


## -description

Gets the index of the icon overlay or the icon image for the specified file with the specified attributes.

## -parameters

### -param pwszPath [in]

Type: <b>PCWSTR</b>

The full path of the file.

### -param dwAttrib

Type: <b>DWORD</b>

The attributes of the file. This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_*) defined in the Windows header files. See <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

### -param pIndex [out]

Type: <b>int*</b>

A pointer to the icon index in the system image list.

### -param dwflags

Type: <b>DWORD</b>

For the index of the icon overlay, use SIOM_OVERLAYINDEX. For the index of the icon image, use SIOM_ICONINDEX.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The appropriate index was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure for any reason.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlaymanager">IShellIconOverlayManager</a>