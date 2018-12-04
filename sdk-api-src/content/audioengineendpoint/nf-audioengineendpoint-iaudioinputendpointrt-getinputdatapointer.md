---
UID: NF:audioengineendpoint.IAudioInputEndpointRT.GetInputDataPointer
title: IAudioInputEndpointRT::GetInputDataPointer
author: windows-sdk-content
description: Gets a pointer to the buffer from which data will be read by the audio engine.
old-location: termserv\iaudioinputendpointrt_getinputdatapointer.htm
tech.root: termserv
ms.assetid: 1da81a49-d421-4643-9be6-b13d45d678f0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetInputDataPointer, GetInputDataPointer method [Remote Desktop Services], GetInputDataPointer method [Remote Desktop Services],IAudioInputEndpointRT interface, IAudioInputEndpointRT interface [Remote Desktop Services],GetInputDataPointer method, IAudioInputEndpointRT.GetInputDataPointer, IAudioInputEndpointRT::GetInputDataPointer, audioengineendpoint/IAudioInputEndpointRT::GetInputDataPointer, termserv.iaudioinputendpointrt_getinputdatapointer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Audioengineendpoint.h
api_name:
 - IAudioInputEndpointRT.GetInputDataPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioInputEndpointRT::GetInputDataPointer


## -description


The <b>GetInputDataPointer</b> method gets a pointer to the buffer from which data will be read by the audio engine.


## -parameters




### -param pConnectionProperty [in, out]

 A pointer to an <a href="https://msdn.microsoft.com/dbf7ed62-445e-4f15-bc21-46117e694dc0">APO_CONNECTION_PROPERTY</a>structure.

The caller sets the member values as follows:

<ul>
<li><b>pBuffer</b> is set to <b>NULL</b>.</li>
<li><b>u32ValidFrameCount</b> contains the number of frames that need to be
    in the retrieved data pointer. The endpoint object must not cache this
    information. The audio engine can change this number depending on
    its processing needs.</li>
<li><b>u32BufferFlags</b> is set to <b>BUFFER_INVALID</b>.</li>
</ul>
If this call completes successfully, the endpoint must set the member values as follows:

<ul>
<li><b>pBuffer</b> points to valid memory where the data has been read. This could include silence depending on the flags that were set in the <b>u32BufferFlags</b> member.</li>
<li><b>u32ValidFrameCount</b> is unchanged.</li>
<li><b>u32BufferFlags</b> is set to <b>BUFFER_VALID</b> if the data pointer contains valid data or to <b>BUFFER_SILENT</b> if the data
    pointer contains only silent data. The data in the buffer does
    not actually need to be silence, but the buffer specified in <b>pBuffer</b> must be capable of holding all the frames of
    silence contained in <b>u32ValidFrameCount</b> to match the required frame count.</li>
</ul>

### -param pAeTimeStamp [in, out]

A pointer to an <a href="https://msdn.microsoft.com/2e239114-1af7-455a-a60f-2054b05e1414">AE_CURRENT_POSITION</a> structure that contains the time stamp of the data that is captured in the buffer.
    This parameter is optional.


## -returns



This method does not return a value.




## -remarks



This method returns a pointer from the endpoint to the buffer <i>pConnectionProperty</i>-&gt;<b>pBuffer</b>, which
    contains data that needs to be passed into the engine as input.
    The data and the buffer pointer must remain valid until the
    <a href="https://msdn.microsoft.com/9dd3f72a-79fe-4d07-a301-d0960e30a2d1">IAudioInputEndpointRT::ReleaseInputDataPointer</a> method is called. The endpoint object must  set  the requested amount of information and insert silence if no
    valid data exists.
    The  buffer pointer, <i>pConnectionProperty</i>-&gt;<b>pBuffer</b>, returned by the endpoint object  must be frame aligned.
    Endpoints do not support the extra space, which may be available in
    the <a href="https://msdn.microsoft.com/dbf7ed62-445e-4f15-bc21-46117e694dc0">APO_CONNECTION_PROPERTY</a> associated with the connection properties
    passed in the <i>pConnectionProperty</i> parameter.

Passing zero in the <b>u32ValidFrameCount</b> member is a valid request. In this case,
    the input pointer must be valid but the endpoint does not read from it. The <i>pConnectionProperty</i>-&gt;<b>u32ValidFrameCount</b>value must be less than or equal to the maximum  frame count supported by the endpoint. To get the supported number of frames, call the <a href="https://msdn.microsoft.com/b9e47262-9e6f-4ddf-a74a-b7fa63983a5a">IAudioEndpoint::GetFramesPerPacket</a> method.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/f9638dea-f61d-45f6-b91d-72e4fc1b4a92">IAudioInputEndpointRT</a>
 

 

