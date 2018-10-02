---
UID: NF:mfidl.IMFSampleGrabberSinkCallback2.OnProcessSampleEx
title: IMFSampleGrabberSinkCallback2::OnProcessSampleEx
author: windows-sdk-content
description: Called when the sample-grabber sink receives a new media sample.
old-location: mf\imfsamplegrabbersinkcallback2_onprocesssampleex.htm
tech.root: MedFound
ms.assetid: dc880967-ac97-4835-bbc9-1bd664e42739
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFSampleGrabberSinkCallback2 interface [Media Foundation],OnProcessSampleEx method, IMFSampleGrabberSinkCallback2.OnProcessSampleEx, IMFSampleGrabberSinkCallback2::OnProcessSampleEx, OnProcessSampleEx, OnProcessSampleEx method [Media Foundation], OnProcessSampleEx method [Media Foundation],IMFSampleGrabberSinkCallback2 interface, mf.imfsamplegrabbersinkcallback2_onprocesssampleex, mfidl/IMFSampleGrabberSinkCallback2::OnProcessSampleEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfidl.h
api_name:
 - IMFSampleGrabberSinkCallback2.OnProcessSampleEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSampleGrabberSinkCallback2::OnProcessSampleEx


## -description


Called when the sample-grabber sink receives a new media sample.


## -parameters




### -param guidMajorMediaType [in]

The major type GUID that specifies the format of the data. For a list of possible values, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Major Media Types</a>.




### -param dwSampleFlags [in]

Sample flags. The sample-grabber sink gets the value of this parameter by calling the <a href="https://msdn.microsoft.com/98e3ed97-cefc-40c2-acda-8b3da74d0d03">IMFSample::GetSampleFlags</a> method of the media sample.


### -param llSampleTime [in]

The presentation time for this sample, in 100-nanosecond units. If the sample does not have a presentation time, the value of this parameter is <b>_I64_MAX</b>


### -param llSampleDuration [in]

The duration of the sample, in 100-nanosecond units.

If the sample does not have a duration, the value of this parameter is <b>_I64_MAX</b>.


### -param pSampleBuffer [in]

A pointer to a buffer that contains the sample data.


### -param dwSampleSize [in]

The size, in bytes, of the <i>pSampleBuffer</i> buffer.


### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. Use this interface to get the attributes for this sample (if any). For a list of sample attributes, see <a href="https://msdn.microsoft.com/64aead5a-61c4-4e83-a556-af33e0aa82be">Sample Attributes</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you use the sample-grabber sink in a playback topology, this method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.




## -see-also




<a href="https://msdn.microsoft.com/b303361b-baaf-4d64-aa5b-a26dd70413f2">IMFSampleGrabberSinkCallback2</a>
 

 

