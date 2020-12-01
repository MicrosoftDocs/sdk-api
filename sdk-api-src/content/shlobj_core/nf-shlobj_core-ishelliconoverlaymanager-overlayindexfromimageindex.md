---
UID: NF:shlobj_core.IShellIconOverlayManager.OverlayIndexFromImageIndex
title: IShellIconOverlayManager::OverlayIndexFromImageIndex (shlobj_core.h)
description: Finds the index of an overlay image for the specified icon image. It can add an overlay if one is not found for the icon.
helpviewer_keywords: ["IShellIconOverlayManager interface [Windows Shell]","OverlayIndexFromImageIndex method","IShellIconOverlayManager.OverlayIndexFromImageIndex","IShellIconOverlayManager::OverlayIndexFromImageIndex","OverlayIndexFromImageIndex","OverlayIndexFromImageIndex method [Windows Shell]","OverlayIndexFromImageIndex method [Windows Shell]","IShellIconOverlayManager interface","_win32_IShellIconOverlayManager_OverlayIndexFromImageIndex","shell.IShellIconOverlayManager_OverlayIndexFromImageIndex","shlobj_core/IShellIconOverlayManager::OverlayIndexFromImageIndex"]
old-location: shell\IShellIconOverlayManager_OverlayIndexFromImageIndex.htm
tech.root: shell
ms.assetid: 7abbdd28-72b8-4a91-81db-6afc1242a086
ms.date: 12/05/2018
ms.keywords: IShellIconOverlayManager interface [Windows Shell],OverlayIndexFromImageIndex method, IShellIconOverlayManager.OverlayIndexFromImageIndex, IShellIconOverlayManager::OverlayIndexFromImageIndex, OverlayIndexFromImageIndex, OverlayIndexFromImageIndex method [Windows Shell], OverlayIndexFromImageIndex method [Windows Shell],IShellIconOverlayManager interface, _win32_IShellIconOverlayManager_OverlayIndexFromImageIndex, shell.IShellIconOverlayManager_OverlayIndexFromImageIndex, shlobj_core/IShellIconOverlayManager::OverlayIndexFromImageIndex
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
 - IShellIconOverlayManager::OverlayIndexFromImageIndex
 - shlobj_core/IShellIconOverlayManager::OverlayIndexFromImageIndex
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
 - IShellIconOverlayManager.OverlayIndexFromImageIndex
---

# IShellIconOverlayManager::OverlayIndexFromImageIndex


## -description

Finds the index of an overlay image for the specified icon image. It can add an overlay if one is not found for the icon.

## -parameters

### -param iImage [in]

Type: <b>int</b>

The existing shell image list index to look for.

### -param piIndex [out]

Type: <b>int</b>

The returned overlay index.

### -param fAdd [in]

Type: <b>BOOL</b>

Whether to add an image if one is not already present.

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
The image index was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An error occurred or the image was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlaymanager">IShellIconOverlayManager</a>