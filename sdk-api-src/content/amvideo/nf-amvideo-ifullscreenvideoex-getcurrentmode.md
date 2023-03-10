---
UID: NF:amvideo.IFullScreenVideoEx.GetCurrentMode
title: IFullScreenVideoEx::GetCurrentMode (amvideo.h)
description: The GetCurrentMode method retrieves the current display mode.
helpviewer_keywords: ["GetCurrentMode","GetCurrentMode method [DirectShow]","GetCurrentMode method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","GetCurrentMode method","IFullScreenVideoEx.GetCurrentMode","IFullScreenVideoEx::GetCurrentMode","IFullScreenVideoGetCurrentMode","amvideo/IFullScreenVideoEx::GetCurrentMode","dshow.ifullscreenvideoex_getcurrentmode"]
old-location: dshow\ifullscreenvideoex_getcurrentmode.htm
tech.root: dshow
ms.assetid: 036914da-4223-4601-9e4a-4c7840b7dd22
ms.date: 12/05/2018
ms.keywords: GetCurrentMode, GetCurrentMode method [DirectShow], GetCurrentMode method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetCurrentMode method, IFullScreenVideoEx.GetCurrentMode, IFullScreenVideoEx::GetCurrentMode, IFullScreenVideoGetCurrentMode, amvideo/IFullScreenVideoEx::GetCurrentMode, dshow.ifullscreenvideoex_getcurrentmode
req.header: amvideo.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFullScreenVideoEx::GetCurrentMode
 - amvideo/IFullScreenVideoEx::GetCurrentMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.GetCurrentMode
---

# IFullScreenVideoEx::GetCurrentMode


## -description

The <code>GetCurrentMode</code> method retrieves the current display mode.

## -parameters

### -param pMode [out]

Pointer to a variable that receives the index of the current video mode. Pass this index to the <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo">IFullScreenVideoEx::GetModeInfo</a> method to obtain information about this mode, including the width, height, and bit depth.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The filter did not load DirectDraw.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>