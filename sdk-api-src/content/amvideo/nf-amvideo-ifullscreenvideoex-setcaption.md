---
UID: NF:amvideo.IFullScreenVideoEx.SetCaption
title: IFullScreenVideoEx::SetCaption (amvideo.h)
description: The SetCaption method sets the caption associated with the full-screen window.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetCaption method","IFullScreenVideoEx.SetCaption","IFullScreenVideoEx::SetCaption","IFullScreenVideoSetCaption","SetCaption","SetCaption method [DirectShow]","SetCaption method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetCaption","dshow.ifullscreenvideoex_setcaption"]
old-location: dshow\ifullscreenvideoex_setcaption.htm
tech.root: dshow
ms.assetid: 6f520ab4-867f-4001-8f2f-25f0d8efe454
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetCaption method, IFullScreenVideoEx.SetCaption, IFullScreenVideoEx::SetCaption, IFullScreenVideoSetCaption, SetCaption, SetCaption method [DirectShow], SetCaption method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetCaption, dshow.ifullscreenvideoex_setcaption
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
 - IFullScreenVideoEx::SetCaption
 - amvideo/IFullScreenVideoEx::SetCaption
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
 - IFullScreenVideoEx.SetCaption
---

# IFullScreenVideoEx::SetCaption


## -description

The <code>SetCaption</code> method sets the caption associated with the full-screen window.

## -parameters

### -param strCaption [in]

String containing the caption.

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
</table>

## -remarks

The caption is visible when the window is minimized.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>