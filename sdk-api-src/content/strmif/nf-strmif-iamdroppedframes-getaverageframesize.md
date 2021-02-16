---
UID: NF:strmif.IAMDroppedFrames.GetAverageFrameSize
title: IAMDroppedFrames::GetAverageFrameSize (strmif.h)
description: The GetAverageFrameSize method retrieves the average size of the frames that the filter has captured.
helpviewer_keywords: ["GetAverageFrameSize","GetAverageFrameSize method [DirectShow]","GetAverageFrameSize method [DirectShow]","IAMDroppedFrames interface","IAMDroppedFrames interface [DirectShow]","GetAverageFrameSize method","IAMDroppedFrames.GetAverageFrameSize","IAMDroppedFrames::GetAverageFrameSize","IAMDroppedFramesGetAverageFrameSize","dshow.iamdroppedframes_getaverageframesize","strmif/IAMDroppedFrames::GetAverageFrameSize"]
old-location: dshow\iamdroppedframes_getaverageframesize.htm
tech.root: dshow
ms.assetid: 49b63a9f-8192-4fce-8cfe-c92bd39ca2b0
ms.date: 12/05/2018
ms.keywords: GetAverageFrameSize, GetAverageFrameSize method [DirectShow], GetAverageFrameSize method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetAverageFrameSize method, IAMDroppedFrames.GetAverageFrameSize, IAMDroppedFrames::GetAverageFrameSize, IAMDroppedFramesGetAverageFrameSize, dshow.iamdroppedframes_getaverageframesize, strmif/IAMDroppedFrames::GetAverageFrameSize
req.header: strmif.h
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
 - IAMDroppedFrames::GetAverageFrameSize
 - strmif/IAMDroppedFrames::GetAverageFrameSize
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
 - IAMDroppedFrames.GetAverageFrameSize
---

# IAMDroppedFrames::GetAverageFrameSize


## -description

The <code>GetAverageFrameSize</code> method retrieves the average size of the frames that the filter has captured.

## -parameters

### -param plAverageSize [out]

Pointer to a variable that receives the average frame size, in bytes, since the filter began streaming.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
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
</table>

## -remarks

If the device does not report a value, the method might succeed but return zero in the <i>plAverageSize</i> parameter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdroppedframes">IAMDroppedFrames Interface</a>