---
UID: NF:strmif.IDVSplitter.DiscardAlternateVideoFrames
title: IDVSplitter::DiscardAlternateVideoFrames
author: windows-sdk-content
description: The DiscardAlternateVideoFrames method discards half of the frames in the video stream. For NTSC, the frame rate is reduced from 30 frames per second (fps) to 15 fps. For PAL, the frame rate is reduced from 25 fps to 12.5 fps.
old-location: dshow\idvsplitter_discardalternatevideoframes.htm
old-project: DirectShow
ms.assetid: 121b94cd-cc39-4ac2-9423-f75df9fcd491
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DiscardAlternateVideoFrames, DiscardAlternateVideoFrames method [DirectShow], DiscardAlternateVideoFrames method [DirectShow],IDVSplitter interface, IDVSplitter interface [DirectShow],DiscardAlternateVideoFrames method, IDVSplitter.DiscardAlternateVideoFrames, IDVSplitter::DiscardAlternateVideoFrames, IDVSplitterDiscardAlternateVideoFrames, dshow.idvsplitter_discardalternatevideoframes, strmif/IDVSplitter::DiscardAlternateVideoFrames
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a7fd27f4-2fc7-4115-b669-b08eed1ec032">IDVSplitter Interface</a>
 

 

