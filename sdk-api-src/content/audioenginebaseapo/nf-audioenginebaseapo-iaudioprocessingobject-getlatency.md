---
UID: NF:audioenginebaseapo.IAudioProcessingObject.GetLatency
title: IAudioProcessingObject::GetLatency
author: windows-sdk-content
description: The GetLatency method returns the latency for this APO. Latency is the amount of time it takes a frame to traverse the processing pass of an APO.
old-location: audio\iaudioprocessingobject_getlatency.htm
tech.root: audio
ms.assetid: 7ac982cd-7fb7-4427-ac17-508bcc72391d
ms.author: windowssdkdev
ms.date: 11/14/2018
ms.keywords: GetLatency, GetLatency method [Audio Devices], GetLatency method [Audio Devices],IAudioProcessingObject interface, IAudioProcessingObject interface [Audio Devices],GetLatency method, IAudioProcessingObject.GetLatency, IAudioProcessingObject::GetLatency, audio.iaudioprocessingobject_getlatency, audio_syseffects_r_51c02d16-7f19-43e9-8656-411abb78ee56.xml, audioenginebaseapo/IAudioProcessingObject::GetLatency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later Windows operating systems.
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
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: Any level
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioenginebaseapo.idl
 - Audioenginebaseapo.idl.dll
api_name:
 - IAudioProcessingObject.GetLatency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- audioenginebaseapo.h
: 
- IAudioProcessingObject.GetLatency
: 
---

# IAudioProcessingObject::GetLatency


## -description


The GetLatency method returns the latency for this APO. Latency is the amount of time it takes a frame to traverse the processing pass of an APO.


## -parameters




### -param pTime [out]

A pointer to an MFTIME structure that will receive the number of units of delay that this APO introduces. Each unit of delay represents 100 nanoseconds.


## -returns



<code>GetLatency</code> returns a value of S_OK if the call was successful. Otherwise, it returns an error code of E_POINTER to indicate that an invalid pointer was passed to the function.




## -remarks



If the client that is calling this APO knows the sampling rate, the client can calculate the latency in terms of the number of frames. To get the total latency of the entire audio signal processing stream, the client must query every APO in the processing chain and add up the results.

<div class="alert"><b>Important</b>    This method is not real-time compliant and must not be called from a real-time processing thread.</div>
<div> </div>


