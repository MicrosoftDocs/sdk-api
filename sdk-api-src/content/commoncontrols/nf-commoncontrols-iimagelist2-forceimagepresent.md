---
UID: NF:commoncontrols.IImageList2.ForceImagePresent
title: IImageList2::ForceImagePresent (commoncontrols.h)
description: Forces an image present, as specified.
helpviewer_keywords: ["ForceImagePresent","ForceImagePresent method [Windows Controls]","ForceImagePresent method [Windows Controls]","IImageList2 interface","IImageList2 interface [Windows Controls]","ForceImagePresent method","IImageList2.ForceImagePresent","IImageList2::ForceImagePresent","ILFIP_ALWAYS","ILFIP_FROMSTANDBY","_shell_IImageList2_ForceImagePresent","_shell_IImageList2_ForceImagePresent_cpp","commoncontrols/IImageList2::ForceImagePresent","controls.IImageList2_ForceImagePresent","controls._shell_IImageList2_ForceImagePresent"]
old-location: controls\IImageList2_ForceImagePresent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\forceimagepresent.htm
ms.date: 12/05/2018
ms.keywords: ForceImagePresent, ForceImagePresent method [Windows Controls], ForceImagePresent method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],ForceImagePresent method, IImageList2.ForceImagePresent, IImageList2::ForceImagePresent, ILFIP_ALWAYS, ILFIP_FROMSTANDBY, _shell_IImageList2_ForceImagePresent, _shell_IImageList2_ForceImagePresent_cpp, commoncontrols/IImageList2::ForceImagePresent, controls.IImageList2_ForceImagePresent, controls._shell_IImageList2_ForceImagePresent
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
 - IImageList2::ForceImagePresent
 - commoncontrols/IImageList2::ForceImagePresent
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
 - IImageList2.ForceImagePresent
---

# IImageList2::ForceImagePresent


## -description

Forces an image present, as specified.

## -parameters

### -param iImage [in]

Type: <b>int</b>

An index of image to force present.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Force image flags. One of the following is valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILFIP_ALWAYS"></a><a id="ilfip_always"></a><dl>
<dt><b>ILFIP_ALWAYS</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Always get the image (can be slow). 

</td>
</tr>
<tr>
<td width="40%"><a id="ILFIP_FROMSTANDBY"></a><a id="ilfip_fromstandby"></a><dl>
<dt><b>ILFIP_FROMSTANDBY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Only get if on standby. 

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.