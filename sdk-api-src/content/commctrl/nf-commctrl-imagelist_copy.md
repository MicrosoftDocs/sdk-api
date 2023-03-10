---
UID: NF:commctrl.ImageList_Copy
title: ImageList_Copy function (commctrl.h)
description: Copies images within a given image list.
helpviewer_keywords: ["ILCF_MOVE","ILCF_SWAP","ImageList_Copy","ImageList_Copy function [Windows Controls]","_win32_ImageList_Copy","_win32_ImageList_Copy_cpp","commctrl/ImageList_Copy","controls.ImageList_Copy","controls._win32_ImageList_Copy"]
old-location: controls\ImageList_Copy.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_copy.htm
ms.date: 12/05/2018
ms.keywords: ILCF_MOVE, ILCF_SWAP, ImageList_Copy, ImageList_Copy function [Windows Controls], _win32_ImageList_Copy, _win32_ImageList_Copy_cpp, commctrl/ImageList_Copy, controls.ImageList_Copy, controls._win32_ImageList_Copy
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
req.dll: Comctl32.dll (version 4.70 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_Copy
 - commctrl/ImageList_Copy
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
 - ImageList_Copy
---

# ImageList_Copy function


## -description

Copies images within a given image list.

## -parameters

### -param himlDst

Type: <b>HIMAGELIST</b>

A handle to an image list that is the target of the copy operation. In current versions of Windows, both <i>himlDst</i> and <i>himlSrc</i> must be identical.

### -param iDst

Type: <b>int</b>

The zero-based index of the image to be used as the destination of the copy operation.

### -param himlSrc

Type: <b>HIMAGELIST</b>

A handle to an image list that is the target of the copy operation. In current versions of Windows, both <i>himlDst</i> and <i>himlSrc</i> must be identical.

### -param iSrc

Type: <b>int</b>

The zero-based index of the image to be used as the source of the copy operation.

### -param uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

the bit flag value that specifies the type of copy operation to be made. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILCF_MOVE"></a><a id="ilcf_move"></a><dl>
<dt><b>ILCF_MOVE</b></dt>
</dl>
</td>
<td width="60%">
The source image is copied to the destination image's index. This operation results in multiple instances of a given image.

</td>
</tr>
<tr>
<td width="40%"><a id="ILCF_SWAP"></a><a id="ilcf_swap"></a><dl>
<dt><b>ILCF_SWAP</b></dt>
</dl>
</td>
<td width="60%">
The source and destination images exchange positions within the image list.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.