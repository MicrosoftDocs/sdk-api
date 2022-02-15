---
UID: NF:commoncontrols.IImageList2.GetOriginalSize
title: IImageList2::GetOriginalSize (commoncontrols.h)
description: Gets the original size of a specified image.
helpviewer_keywords: ["GetOriginalSize","GetOriginalSize method [Windows Controls]","GetOriginalSize method [Windows Controls]","IImageList2 interface","IImageList2 interface [Windows Controls]","GetOriginalSize method","IImageList2.GetOriginalSize","IImageList2::GetOriginalSize","ILGOS_ALWAYS","ILGOS_FROMSTANDBY","_shell_IImageList2_GetOriginalSize","_shell_IImageList2_GetOriginalSize_cpp","commoncontrols/IImageList2::GetOriginalSize","controls.IImageList2_GetOriginalSize","controls._shell_IImageList2_GetOriginalSize"]
old-location: controls\IImageList2_GetOriginalSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\getoriginalsize.htm
ms.date: 12/05/2018
ms.keywords: GetOriginalSize, GetOriginalSize method [Windows Controls], GetOriginalSize method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],GetOriginalSize method, IImageList2.GetOriginalSize, IImageList2::GetOriginalSize, ILGOS_ALWAYS, ILGOS_FROMSTANDBY, _shell_IImageList2_GetOriginalSize, _shell_IImageList2_GetOriginalSize_cpp, commoncontrols/IImageList2::GetOriginalSize, controls.IImageList2_GetOriginalSize, controls._shell_IImageList2_GetOriginalSize
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
 - IImageList2::GetOriginalSize
 - commoncontrols/IImageList2::GetOriginalSize
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
 - IImageList2.GetOriginalSize
---

# IImageList2::GetOriginalSize


## -description

Gets the original size of a specified image.

## -parameters

### -param iImage [in]

Type: <b>int</b>

The index of desired image.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flags for getting original size. One of the following is valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILGOS_ALWAYS"></a><a id="ilgos_always"></a><dl>
<dt><b>ILGOS_ALWAYS</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Always get the original size (can be slow). 

</td>
</tr>
<tr>
<td width="40%"><a id="ILGOS_FROMSTANDBY"></a><a id="ilgos_fromstandby"></a><dl>
<dt><b>ILGOS_FROMSTANDBY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Only get if present or on standby. 

</td>
</tr>
</table>

### -param pcx [out]

Type: <b>int*</b>

A pointer to the x-axis count.

### -param pcy [out]

Type: <b>int*</b>

A pointer to the y-axis count.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.