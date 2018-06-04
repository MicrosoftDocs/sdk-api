---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IETFilter::SetRecordingOn


## -description


The <b>SetRecordingOn</b> method signals to the Encrypter/Tagger filter that the Video Control is about to start or stop recording.


## -parameters




### -param fRecState

<b>TRUE</b> if recording is about to start, or <b>FALSE</b> if recording is about to stop.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



The <b>SetRecordingOn</b> method enables the Video Control to enforce copy protection in the television broadcast signal. When the Video Control uses the Stream Buffer Engine to play television content, the Encrypter/Tagger filter is located in the Stream Buffer Sink graph. The Encrypter/Tagger sends data to the Stream Buffer Sink for both playback and recording. When <b>SetRecordingOn</b> is called with the value <b>TRUE</b>, the Encrypter/Tagger watches the video stream for the copy protection flags and sends a broadcast event if they change. The Video Control listens for the event and disallows the recording if indicated by the copy protection flag.




## -see-also




<a href="https://msdn.microsoft.com/9fce6b33-394c-47d2-9d02-7b0dadaa1736">IETFilter Interface</a>
 

 

