---
UID: NF:commctrl.ImageList_WriteEx
title: ImageList_WriteEx function (commctrl.h)
description: Writes an image list to a stream. (ImageList_WriteEx)
helpviewer_keywords: ["ILP_DOWNLEVEL","ILP_NORMAL","ImageList_WriteEx","ImageList_WriteEx function [Windows Controls]","_win32_ImageList_WriteEx","_win32_ImageList_WriteEx_cpp","commctrl/ImageList_WriteEx","controls.ImageList_WriteEx","controls._win32_ImageList_WriteEx"]
old-location: controls\ImageList_WriteEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_writeex.htm
ms.date: 12/05/2018
ms.keywords: ILP_DOWNLEVEL, ILP_NORMAL, ImageList_WriteEx, ImageList_WriteEx function [Windows Controls], _win32_ImageList_WriteEx, _win32_ImageList_WriteEx_cpp, commctrl/ImageList_WriteEx, controls.ImageList_WriteEx, controls._win32_ImageList_WriteEx
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
 - ImageList_WriteEx
 - commctrl/ImageList_WriteEx
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
 - ImageList_WriteEx
---

# ImageList_WriteEx function


## -description

Writes an image list to a stream.

## -parameters

### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A flag that specifies how the stream is written.



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
Writes to the stream using the file format for <a href="/windows/desktop/Controls/common-control-versions">Common Controls 6.0</a>, which includes information about image list attributes new to this version.  
			

</td>
</tr>
<tr>
<td width="40%"><a id="ILP_DOWNLEVEL"></a><a id="ilp_downlevel"></a><dl>
<dt><b>ILP_DOWNLEVEL</b></dt>
</dl>
</td>
<td width="60%">
Writes to the stream using a file format previous to version 6.0.  Specify this flag if you need to save image lists loaded under Common Controls versions earlier than version 6.0.
			

</td>
</tr>
</table>

### -param pstm [in]

Type: <b>LPSTREAM</b>

The address of the stream.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You should not create an image list that is written with the ILP_DOWNLEVEL flag with <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_create">ILC_COLOR32</a>.  
	

To use <b>ImageList_WriteEx</b>, the application must specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_read">ImageList_Read</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_readex">ImageList_ReadEx</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_write">ImageList_Write</a>



<b>Reference</b>
