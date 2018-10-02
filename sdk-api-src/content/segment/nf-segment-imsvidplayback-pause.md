---
UID: NF:segment.IMSVidPlayback.Pause
title: IMSVidPlayback::Pause
author: windows-sdk-content
description: The Pause method pauses the playback device.
old-location: mstv\imsvidplayback_pause.htm
tech.root: MSTV
ms.assetid: 430528b7-3b3a-4df9-8093-9b0f9262f106
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Pause method, IMSVidPlayback.Pause, IMSVidPlayback::Pause, IMSVidPlaybackPause, Pause, Pause method [Microsoft TV Technologies], Pause method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_pause, segment/IMSVidPlayback::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidPlayback.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidPlayback::Pause


## -description


The <b>Pause</b> method pauses the playback device.

Applications should call the <a href="https://msdn.microsoft.com/fd7687d8-325f-4a51-ab57-ffcc45a9157b">IMSVidCtl::Pause</a> method, rather than this method.


## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method allows for direct control of the source. However, if the underlying source filter is controlled using the standard DirectShow <a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl</a> interface, this method returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 

