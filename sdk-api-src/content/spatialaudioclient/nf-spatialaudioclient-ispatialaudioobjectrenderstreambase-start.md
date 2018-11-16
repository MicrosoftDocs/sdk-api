---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.Start
title: ISpatialAudioObjectRenderStreamBase::Start
author: windows-sdk-content
description: Starts the spatial audio stream.
old-location: coreaudio\ispatialaudioobjectrenderstream_start.htm
tech.root: CoreAudio
ms.assetid: 25D968AC-F5D2-4CAB-87ED-29FC63E5A5A4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase interface [Core Audio],Start method, ISpatialAudioObjectRenderStreamBase.Start, ISpatialAudioObjectRenderStreamBase::Start, Start, Start method [Core Audio], Start method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, coreaudio.ispatialaudioobjectrenderstream_start, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Start
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- spatialaudioclient.h
: 
- ISpatialAudioObjectRenderStreamBase.Start
: 
---

# ISpatialAudioObjectRenderStreamBase::Start


## -description


Starts the spatial audio stream.  


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_STREAM_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been stopped. Stop the stream by calling <a href="https://msdn.microsoft.com/d5824aa9-0b91-4bee-9c0c-26e12a6b96b5">Stop</a>.

</td>
</tr>
</table>
 




## -remarks



Starting the stream causes data flow between the endpoint buffer and the audio engine.  
    The first time this method is called, the stream's audio clock position will be at 0.  
    Otherwise, the clock resumes from its position at the time that the stream was last paused with a call to <a href="https://msdn.microsoft.com/6ECD17AB-C37D-4F4E-9D7F-EC48FC3B838C">Stop</a>.  
Call <a href="https://msdn.microsoft.com/F6F096C0-3384-4463-B25F-99C6A7B3263B">Reset</a> to  reset the clock position to 0 and cause all active <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> instances to be revoked. 

The stream must have been previously stopped with a call to <a href="https://msdn.microsoft.com/6ECD17AB-C37D-4F4E-9D7F-EC48FC3B838C">Stop</a> or the method will fail and return SPTLAUDCLNT_E_STREAM_NOT_STOPPED.




## -see-also




<a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/2C2BE871-EFD1-40E1-B466-6BBD09C56852">ISpatialAudioObjectRenderStreamBase</a>
 

 

