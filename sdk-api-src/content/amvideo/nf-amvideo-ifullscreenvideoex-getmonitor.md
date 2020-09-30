---
UID: NF:amvideo.IFullScreenVideoEx.GetMonitor
title: IFullScreenVideoEx::GetMonitor (amvideo.h)
description: The GetMonitor method queries which monitor the Full Screen Renderer is using. The Full Screen Renderer only supports the primary monitor, so the returned value is always zero.
helpviewer_keywords: ["GetMonitor","GetMonitor method [DirectShow]","GetMonitor method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","GetMonitor method","IFullScreenVideoEx.GetMonitor","IFullScreenVideoEx::GetMonitor","IFullScreenVideoGetMonitor","amvideo/IFullScreenVideoEx::GetMonitor","dshow.ifullscreenvideoex_getmonitor"]
old-location: dshow\ifullscreenvideoex_getmonitor.htm
tech.root: dshow
ms.assetid: 18825029-2035-46b3-a6a5-9edd8e0437c6
ms.date: 12/05/2018
ms.keywords: GetMonitor, GetMonitor method [DirectShow], GetMonitor method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetMonitor method, IFullScreenVideoEx.GetMonitor, IFullScreenVideoEx::GetMonitor, IFullScreenVideoGetMonitor, amvideo/IFullScreenVideoEx::GetMonitor, dshow.ifullscreenvideoex_getmonitor
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
 - IFullScreenVideoEx::GetMonitor
 - amvideo/IFullScreenVideoEx::GetMonitor
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
 - IFullScreenVideoEx.GetMonitor
---

# IFullScreenVideoEx::GetMonitor


## -description

The <code>GetMonitor</code> method queries which monitor the Full Screen Renderer is using. The Full Screen Renderer only supports the primary monitor, so the returned value is always zero.

## -parameters

### -param Monitor [out]

Pointer to a variable that receives the index of the monitor.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>