---
UID: NF:commoncontrols.IImageList2.Replace2
title: IImageList2::Replace2 (commoncontrols.h)
description: Replaces an image in an image list.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","Replace2 method","IImageList2.Replace2","IImageList2::Replace2","ILR_DEFAULT","ILR_HORIZONTAL_CENTER","ILR_HORIZONTAL_LEFT","ILR_HORIZONTAL_RIGHT","ILR_SCALE_ASPECTRATIO","ILR_SCALE_CLIP","ILR_VERTICAL_BOTTOM","ILR_VERTICAL_CENTER","ILR_VERTICAL_TOP","Replace2","Replace2 method [Windows Controls]","Replace2 method [Windows Controls]","IImageList2 interface","_shell_IImageList2_Replace2","_shell_IImageList2_Replace2_cpp","commoncontrols/IImageList2::Replace2","controls.IImageList2_Replace2","controls._shell_IImageList2_Replace2"]
old-location: controls\IImageList2_Replace2.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\replace2.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],Replace2 method, IImageList2.Replace2, IImageList2::Replace2, ILR_DEFAULT, ILR_HORIZONTAL_CENTER, ILR_HORIZONTAL_LEFT, ILR_HORIZONTAL_RIGHT, ILR_SCALE_ASPECTRATIO, ILR_SCALE_CLIP, ILR_VERTICAL_BOTTOM, ILR_VERTICAL_CENTER, ILR_VERTICAL_TOP, Replace2, Replace2 method [Windows Controls], Replace2 method [Windows Controls],IImageList2 interface, _shell_IImageList2_Replace2, _shell_IImageList2_Replace2_cpp, commoncontrols/IImageList2::Replace2, controls.IImageList2_Replace2, controls._shell_IImageList2_Replace2
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList2::Replace2
 - commoncontrols/IImageList2::Replace2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.Replace2
---

# IImageList2::Replace2


## -description

Replaces an image in an image list.

## -parameters

### -param i [in]

Type: <b>int</b>

The index of the image to replace.

### -param hbmImage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the image.

### -param hbmMask [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored.

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies how the mask is applied to the image as one or a bitwise combination of the following decoration flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILR_DEFAULT"></a><a id="ilr_default"></a><dl>
<dt><b>ILR_DEFAULT</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_HORIZONTAL_LEFT"></a><a id="ilr_horizontal_left"></a><dl>
<dt><b>ILR_HORIZONTAL_LEFT</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Horizontally align to left.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_HORIZONTAL_CENTER"></a><a id="ilr_horizontal_center"></a><dl>
<dt><b>ILR_HORIZONTAL_CENTER</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Horizontally center.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_HORIZONTAL_RIGHT"></a><a id="ilr_horizontal_right"></a><dl>
<dt><b>ILR_HORIZONTAL_RIGHT</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Horizontally align to right.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_VERTICAL_TOP"></a><a id="ilr_vertical_top"></a><dl>
<dt><b>ILR_VERTICAL_TOP</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Vertically align to top.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_VERTICAL_CENTER"></a><a id="ilr_vertical_center"></a><dl>
<dt><b>ILR_VERTICAL_CENTER</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Vertically align to center.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_VERTICAL_BOTTOM"></a><a id="ilr_vertical_bottom"></a><dl>
<dt><b>ILR_VERTICAL_BOTTOM</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Vertically align to bottom.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_SCALE_CLIP"></a><a id="ilr_scale_clip"></a><dl>
<dt><b>ILR_SCALE_CLIP</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Do nothing.

</td>
</tr>
<tr>
<td width="40%"><a id="ILR_SCALE_ASPECTRATIO"></a><a id="ilr_scale_aspectratio"></a><dl>
<dt><b>ILR_SCALE_ASPECTRATIO</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Scale.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.