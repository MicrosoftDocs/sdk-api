---
UID: NF:audioengineendpoint.IAudioOutputEndpointRT.GetOutputDataPointer
title: IAudioOutputEndpointRT::GetOutputDataPointer
author: windows-sdk-content
description: Returns a pointer to the output buffer in which data will be written by the audio engine.
old-location: termserv\iaudiooutputendpointrt_getoutputdatapointer.htm
tech.root: termserv
ms.assetid: 14d69520-3d0c-42ee-8986-9d83b5cff62e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOutputDataPointer, GetOutputDataPointer method [Remote Desktop Services], GetOutputDataPointer method [Remote Desktop Services],IAudioOutputEndpointRT interface, IAudioOutputEndpointRT interface [Remote Desktop Services],GetOutputDataPointer method, IAudioOutputEndpointRT.GetOutputDataPointer, IAudioOutputEndpointRT::GetOutputDataPointer, audioengineendpoint/IAudioOutputEndpointRT::GetOutputDataPointer, termserv.iaudiooutputendpointrt_getoutputdatapointer
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
 - IAudioOutputEndpointRT.GetOutputDataPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioOutputEndpointRT::GetOutputDataPointer


## -description


The <b>GetOutputDataPointer</b> method returns a pointer to the output buffer in which data will be written by the audio engine.


## -parameters




### -param u32FrameCount [in]

The number of frames in the output buffer pointed to by the data pointer that is returned by this method. The endpoint must not
    cache this information because this can be changed by the audio engine depending on its processing requirements. For more information, see Remarks.


### -param pAeTimeStamp [in]

A pointer to an <a href="https://msdn.microsoft.com/2e239114-1af7-455a-a60f-2054b05e1414">AE_CURRENT_POSITION</a> structure that specifies the time stamp of the data that is rendered. This parameter is optional.


## -returns



A pointer to the buffer to which data will be written.




## -remarks



This method returns a pointer to a buffer in which the audio engine writes data.
    The data is not valid until the <a href="https://msdn.microsoft.com/55b7d55e-b684-4c6e-a937-e8922732857d">IAudioOutputEndpointRT::ReleaseOutputDataPointer</a> method is called.
    The returned pointer must be frame-aligned.

The frame count passed in <b>u32FrameCount</b>  must be less than or equal to the maximum number of frames supported by the endpoint. To get the maximum frame count that the endpoint can support, the audio engine calls the <a href="https://msdn.microsoft.com/b9e47262-9e6f-4ddf-a74a-b7fa63983a5a">IAudioEndpoint::GetFramesPerPacket</a> method.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/b881b2f9-ffe9-46ff-94aa-eef0af172a3e">IAudioOutputEndpointRT</a>
 

 

