---
UID: NF:encdec.IETFilter.SetRecordingOn
title: IETFilter::SetRecordingOn
author: windows-sdk-content
description: The SetRecordingOn method signals to the Encrypter/Tagger filter that the Video Control is about to start or stop recording.
old-location: mstv\ietfilter_setrecordingon.htm
old-project: mstv
ms.assetid: 4579b897-8b68-4b95-8dd4-e5fd94195742
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IETFilter interface [Microsoft TV Technologies],SetRecordingOn method, IETFilter.SetRecordingOn, IETFilter::SetRecordingOn, IETFilterSetRecordingOn, SetRecordingOn, SetRecordingOn method [Microsoft TV Technologies], SetRecordingOn method [Microsoft TV Technologies],IETFilter interface, encdec/IETFilter::SetRecordingOn, mstv.ietfilter_setrecordingon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilter.SetRecordingOn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

