---
UID: NF:strmif.IDVSplitter.DiscardAlternateVideoFrames
title: IDVSplitter::DiscardAlternateVideoFrames (strmif.h)
author: windows-sdk-content
description: The DiscardAlternateVideoFrames method discards half of the frames in the video stream. For NTSC, the frame rate is reduced from 30 frames per second (fps) to 15 fps. For PAL, the frame rate is reduced from 25 fps to 12.5 fps.
old-location: dshow\idvsplitter_discardalternatevideoframes.htm
tech.root: DirectShow
ms.assetid: 121b94cd-cc39-4ac2-9423-f75df9fcd491
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DiscardAlternateVideoFrames, DiscardAlternateVideoFrames method [DirectShow], DiscardAlternateVideoFrames method [DirectShow],IDVSplitter interface, IDVSplitter interface [DirectShow],DiscardAlternateVideoFrames method, IDVSplitter.DiscardAlternateVideoFrames, IDVSplitter::DiscardAlternateVideoFrames, IDVSplitterDiscardAlternateVideoFrames, dshow.idvsplitter_discardalternatevideoframes, strmif/IDVSplitter::DiscardAlternateVideoFrames
ms.topic: method
f1_keywords: 
 - "strmif/IDVSplitter.DiscardAlternateVideoFrames"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IDVSplitter.DiscardAlternateVideoFrames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVSplitter::DiscardAlternateVideoFrames


## -description



The <b>DiscardAlternateVideoFrames</b> method discards half of the frames in the video stream. For NTSC, the frame rate is reduced from 30 frames per second (fps) to 15 fps. For PAL, the frame rate is reduced from 25 fps to 12.5 fps.




## -parameters




### -param nDiscard [in]

Flag that specifies whether to discard frames. If the value is non-zero, the filter discards alternate frames. If the value is zero, the filter delivers every frame.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Filter is paused or running.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvsplitter">IDVSplitter Interface</a>
 

 

