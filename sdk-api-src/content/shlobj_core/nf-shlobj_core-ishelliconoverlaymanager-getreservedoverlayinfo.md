---
UID: NF:shlobj_core.IShellIconOverlayManager.GetReservedOverlayInfo
title: IShellIconOverlayManager::GetReservedOverlayInfo (shlobj_core.h)
description: Gets the index of the icon overlay or the icon image for the specified file with the specified attributes from one of the reserved overlays.
helpviewer_keywords: ["GetReservedOverlayInfo","GetReservedOverlayInfo method [Windows Shell]","GetReservedOverlayInfo method [Windows Shell]","IShellIconOverlayManager interface","IShellIconOverlayManager interface [Windows Shell]","GetReservedOverlayInfo method","IShellIconOverlayManager.GetReservedOverlayInfo","IShellIconOverlayManager::GetReservedOverlayInfo","_win32_IShellIconOverlayManager_GetReservedOverlayInfo","shell.IShellIconOverlayManager_GetReservedOverlayInfo","shlobj_core/IShellIconOverlayManager::GetReservedOverlayInfo"]
old-location: shell\IShellIconOverlayManager_GetReservedOverlayInfo.htm
tech.root: shell
ms.assetid: 052e1648-359c-4202-a3ca-c5bd8a7e54e5
ms.date: 12/05/2018
ms.keywords: GetReservedOverlayInfo, GetReservedOverlayInfo method [Windows Shell], GetReservedOverlayInfo method [Windows Shell],IShellIconOverlayManager interface, IShellIconOverlayManager interface [Windows Shell],GetReservedOverlayInfo method, IShellIconOverlayManager.GetReservedOverlayInfo, IShellIconOverlayManager::GetReservedOverlayInfo, _win32_IShellIconOverlayManager_GetReservedOverlayInfo, shell.IShellIconOverlayManager_GetReservedOverlayInfo, shlobj_core/IShellIconOverlayManager::GetReservedOverlayInfo
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
 - IShellIconOverlayManager::GetReservedOverlayInfo
 - shlobj_core/IShellIconOverlayManager::GetReservedOverlayInfo
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
 - IShellIconOverlayManager.GetReservedOverlayInfo
---

# IShellIconOverlayManager::GetReservedOverlayInfo


## -description

Gets the index of the icon overlay or the icon image for the specified file with the specified attributes from one of the reserved overlays.

## -parameters

### -param pwszPath [in, optional]

Type: <b>PCWSTR</b>

The full path of the file.

### -param dwAttrib

Type: <b>DWORD</b>

The attributes of the file. This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_*) defined in the Windows header files. See <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

### -param pIndex [out]

Type: <b>int*</b>

The index of the icon image or icon overlay, depending on the value of <i>dwflags</i>.

### -param dwflags

Type: <b>DWORD</b>

For the index of the icon overlay, use SIOM_OVERLAYINDEX. For the index of the icon image, use SIOM_ICONINDEX.

### -param iReservedID

Type: <b>int</b>

The reserved icon overlay ID.

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
Failure, for any reason.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlaymanager">IShellIconOverlayManager</a>