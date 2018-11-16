---
UID: NF:segment.IMSVidStreamBufferSink.get_ContentRecorder
title: IMSVidStreamBufferSink::get_ContentRecorder
author: windows-sdk-content
description: The get_ContentRecorder method creates a new content recording object.
old-location: mstv\imsvidstreambuffersink_get_contentrecorder.htm
tech.root: mstv
ms.assetid: 9fecdf37-0ad2-499b-8604-5e60bb0aa6e2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],get_ContentRecorder method, IMSVidStreamBufferSink.get_ContentRecorder, IMSVidStreamBufferSink::get_ContentRecorder, IMSVidStreamBufferSinkget_ContentRecorder, get_ContentRecorder, get_ContentRecorder method [Microsoft TV Technologies], get_ContentRecorder method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_get_contentrecorder, segment/IMSVidStreamBufferSink::get_ContentRecorder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMSVidStreamBufferSink.get_ContentRecorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidStreamBufferSink.get_ContentRecorder
: 
---

# IMSVidStreamBufferSink::get_ContentRecorder


## -description


The <b>get_ContentRecorder</b> method creates a new content recording object.


## -parameters




### -param pszFilename [in]

Specifies the name of the file to hold the recording.


### -param pRecordingIUnknown [out]

Receives a pointer to the recording object's <a href="https://msdn.microsoft.com/a61414dc-a9a0-4c65-8f5a-eaabc79783e3">IMSVidStreamBufferRecordingControl</a> interface.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The caller must release the returned <a href="https://msdn.microsoft.com/a61414dc-a9a0-4c65-8f5a-eaabc79783e3">IMSVidStreamBufferRecordingControl</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/80f6cd3a-8cb8-4bda-9b66-33e7d214015a">IMSVidStreamBufferSink Interface</a>
 

 

