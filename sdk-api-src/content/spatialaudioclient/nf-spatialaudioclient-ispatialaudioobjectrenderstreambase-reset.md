---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.Reset
title: ISpatialAudioObjectRenderStreamBase::Reset (spatialaudioclient.h)
author: windows-sdk-content
description: Reset a stopped audio stream.
old-location: coreaudio\ispatialaudioobjectrenderstream_reset.htm
tech.root: CoreAudio
ms.assetid: F6F096C0-3384-4463-B25F-99C6A7B3263B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase interface [Core Audio],Reset method, ISpatialAudioObjectRenderStreamBase.Reset, ISpatialAudioObjectRenderStreamBase::Reset, Reset, Reset method [Core Audio], Reset method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, coreaudio.ispatialaudioobjectrenderstream_reset, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Reset
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
 - ISpatialAudioObjectRenderStreamBase.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectRenderStreamBase::Reset


## -description


Reset a stopped audio stream.   
      



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



Resetting the audio stream flushes all pending data and resets the audio clock stream position to 0. Resetting the stream also causes all active <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> instances to be revoked.  
    A subsequent call to <a href="https://msdn.microsoft.com/25D968AC-F5D2-4CAB-87ED-29FC63E5A5A4">Start</a> causes the stream to start from 0 position.  

The stream must have been previously stopped with a call to <a href="https://msdn.microsoft.com/6ECD17AB-C37D-4F4E-9D7F-EC48FC3B838C">Stop</a> or the method will fail and return SPTLAUDCLNT_E_STREAM_NOT_STOPPED.




## -see-also




<a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a>
 

 

