---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.Stop
title: ISpatialAudioObjectRenderStreamBase::Stop (spatialaudioclient.h)
author: windows-sdk-content
description: Stops a running audio stream.
old-location: coreaudio\ispatialaudioobjectrenderstream_stop.htm
tech.root: CoreAudio
ms.assetid: 6ECD17AB-C37D-4F4E-9D7F-EC48FC3B838C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase interface [Core Audio],Stop method, ISpatialAudioObjectRenderStreamBase.Stop, ISpatialAudioObjectRenderStreamBase::Stop, Stop, Stop method [Core Audio], Stop method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, coreaudio.ispatialaudioobjectrenderstream_stop, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Stop
ms.topic: method
f1_keywords: 
 - "spatialaudioclient/ISpatialAudioObjectRenderStreamBase.Stop"
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
 - ISpatialAudioObjectRenderStreamBase.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioObjectRenderStreamBase::Stop


## -description


Stops a running audio stream.   


## -parameters






## -returns



If the method succeeds, it returns S_OK. If the stream is not running when this method is called, it returns S_FALSE.




## -remarks



 Stopping stream causes data to stop flowing between the endpoint buffer and the audio engine.  
    You can consider this operation to pause the stream because it leaves the stream's audio clock at its current stream position and does not reset it to 0. A subsequent call to <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start">Start</a> causes the stream to resume running from the current position.  
    Call <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset">Reset</a> to  reset the clock position to 0 and cause all active <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> instances to be revoked.  





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a>
 

 

