---
UID: NF:commctrl.ImageList_ReadEx
title: ImageList_ReadEx function (commctrl.h)
description: Reads an image list from a stream, and returns an IImageList interface to the image list.
helpviewer_keywords: ["ILP_DOWNLEVEL","ILP_NORMAL","ImageList_ReadEx","ImageList_ReadEx function [Windows Controls]","_win32_ImageList_ReadEx","_win32_ImageList_ReadEx_cpp","commctrl/ImageList_ReadEx","controls.ImageList_ReadEx","controls._win32_ImageList_ReadEx"]
old-location: controls\ImageList_ReadEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_readex.htm
ms.date: 12/05/2018
ms.keywords: ILP_DOWNLEVEL, ILP_NORMAL, ImageList_ReadEx, ImageList_ReadEx function [Windows Controls], _win32_ImageList_ReadEx, _win32_ImageList_ReadEx_cpp, commctrl/ImageList_ReadEx, controls.ImageList_ReadEx, controls._win32_ImageList_ReadEx
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_ReadEx
 - commctrl/ImageList_ReadEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_ReadEx
---

# ImageList_ReadEx function


## -description

Reads an image list from a stream, and returns an <a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist">IImageList</a> interface to the image list.

## -parameters

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A flag that specifies how the stream is read.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILP_NORMAL"></a><a id="ilp_normal"></a><dl>
<dt><b>ILP_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Expects an image list that was written with the ILP_NORMAL flag specified.
			

</td>
</tr>
<tr>
<td width="40%"><a id="ILP_DOWNLEVEL"></a><a id="ilp_downlevel"></a><dl>
<dt><b>ILP_DOWNLEVEL</b></dt>
</dl>
</td>
<td width="60%">
Expects an image list that was written with the ILP_DOWNLEVEL flag specified.
			

</td>
</tr>
</table>

### -param pstm [in]

Type: <b>LPSTREAM</b>

The address of the stream.

### -param riid [out]

Type: <b>REFIID</b>

An IID for the image list.

### -param ppv [out]

Type: <b>void**</b>

The address of a pointer to the interface for the image list if successful, <b>NULL</b> otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>ImageList_ReadEx</b>, the application must specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_read">ImageList_Read</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_write">ImageList_Write</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_writeex">ImageList_WriteEx</a>



<b>Reference</b>