---
UID: NF:shlobj_core.IShellIconOverlay.GetOverlayIconIndex
title: IShellIconOverlay::GetOverlayIconIndex (shlobj_core.h)
description: Gets the index of the icon overlay in the system image list.
helpviewer_keywords: ["GetOverlayIconIndex","GetOverlayIconIndex method [Windows Shell]","GetOverlayIconIndex method [Windows Shell]","IShellIconOverlay interface","IShellIconOverlay interface [Windows Shell]","GetOverlayIconIndex method","IShellIconOverlay.GetOverlayIconIndex","IShellIconOverlay::GetOverlayIconIndex","_win32_IShellIconOverlay_GetOverlayIconIndex","shell.IShellIconOverlay_GetOverlayIconIndex","shlobj_core/IShellIconOverlay::GetOverlayIconIndex"]
old-location: shell\IShellIconOverlay_GetOverlayIconIndex.htm
tech.root: shell
ms.assetid: ae7c55a1-8540-44d3-9793-2d6ac849ef60
ms.date: 12/05/2018
ms.keywords: GetOverlayIconIndex, GetOverlayIconIndex method [Windows Shell], GetOverlayIconIndex method [Windows Shell],IShellIconOverlay interface, IShellIconOverlay interface [Windows Shell],GetOverlayIconIndex method, IShellIconOverlay.GetOverlayIconIndex, IShellIconOverlay::GetOverlayIconIndex, _win32_IShellIconOverlay_GetOverlayIconIndex, shell.IShellIconOverlay_GetOverlayIconIndex, shlobj_core/IShellIconOverlay::GetOverlayIconIndex
req.header: shlobj_core.h
req.include-header: 
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
 - IShellIconOverlay::GetOverlayIconIndex
 - shlobj_core/IShellIconOverlay::GetOverlayIconIndex
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
 - IShellIconOverlay.GetOverlayIconIndex
---

# IShellIconOverlay::GetOverlayIconIndex


## -description

Gets the index of the icon overlay in the system image list.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

Pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that identifies the object whose icon is being displayed.

### -param pIconIndex [in, out]

Type: <b>int*</b>

Pointer to the index of the icon overlay's image in the system image list. This index is equivalent to the <i>iImage</i> value that is specified when you add an overlay image to a private image list with the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_setoverlayimage">ImageList::SetOverlayImage</a> function.

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
The index of an overlay was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No overlay exists for this file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The PIDL is invalid.

</td>
</tr>
</table>

## -remarks

To retrieve the overlay's image index in the system image list, you must first call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa">SHGetIconOverlayIndex</a> to retrieve the overlay index. Then use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro to convert the overlay index into the equivalent image index.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>