---
UID: NF:strmif.IAMDroppedFrames.GetNumDropped
title: IAMDroppedFrames::GetNumDropped (strmif.h)
description: The GetNumDropped method retrieves the total number of frames that the filter has dropped since it started streaming.helpviewer_keywords: ["GetNumDropped","GetNumDropped method [DirectShow]","GetNumDropped method [DirectShow]","IAMDroppedFrames interface","IAMDroppedFrames interface [DirectShow]","GetNumDropped method","IAMDroppedFrames.GetNumDropped","IAMDroppedFrames::GetNumDropped","IAMDroppedFramesGetNumDropped","dshow.iamdroppedframes_getnumdropped","strmif/IAMDroppedFrames::GetNumDropped"]
old-location: dshow\iamdroppedframes_getnumdropped.htm
tech.root: DirectShow
ms.assetid: d7e91efb-0755-4319-ac85-abc6ecdc3e2a
ms.date: 12/05/2018
ms.keywords: GetNumDropped, GetNumDropped method [DirectShow], GetNumDropped method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetNumDropped method, IAMDroppedFrames.GetNumDropped, IAMDroppedFrames::GetNumDropped, IAMDroppedFramesGetNumDropped, dshow.iamdroppedframes_getnumdropped, strmif/IAMDroppedFrames::GetNumDropped
f1_keywords:
- strmif/IAMDroppedFrames.GetNumDropped
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMDroppedFrames.GetNumDropped
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDroppedFrames::GetNumDropped


## -description



The <code>GetNumDropped</code> method retrieves the total number of frames that the filter has dropped since it started streaming.




## -parameters




### -param plDropped [out]

Pointer to a variable that receives the number of dropped frames.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



The filter resets the count to zero when it transitions from stopped to paused.

If your application uses the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl</a> interface to control a pin, the driver might continue to count dropped and non-dropped frames while the pin is off. To get an accurate count, call this method once when you turn on the pin, and again when you turn off the pin. The difference is the total number of dropped frames. (If the start time occurs later than the call to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-startat">IAMStreamControl::StartAt</a>, the application should listen for the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-stream-control-started">EC_STREAM_CONTROL_STARTED</a> event.) These remarks also apply if your application uses the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-controlstream">ICaptureGraphBuilder2::ControlStream</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdroppedframes">IAMDroppedFrames Interface</a>
 

 

