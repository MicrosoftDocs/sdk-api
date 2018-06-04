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

# _MF_TRANSCODE_SINK_INFO structure


## -description


Contains information about the audio and video streams for the transcode sink activation object.

To get the information stored in this structure, call <a href="https://msdn.microsoft.com/d880e13a-879e-4882-a69d-f1920225e478">IMFTranscodeSinkInfoProvider::GetSinkInfo</a>.


## -struct-fields




### -field dwVideoStreamID

The stream identifier of the video stream.


### -field pVideoMediaType

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type for the  video stream. This member can be <b>NULL</b>.


### -field dwAudioStreamID

The stream identifier of the audio stream.


### -field pAudioMediaType

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type for the  audio stream. This member can be <b>NULL</b>.


## -remarks



The <a href="https://msdn.microsoft.com/d880e13a-879e-4882-a69d-f1920225e478">IMFTranscodeSinkInfoProvider::GetSinkInfo</a> method assigns <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> pointers to the <b>pAudioMediaType</b> and <b>pVideoMediaType</b> members of this structure. The method might set either member to <b>NULL</b>. If either member is non-<b>NULL</b> after the method returns, the caller must release the <b>IMFMediaType</b> pointers.




## -see-also




<a href="https://msdn.microsoft.com/d880e13a-879e-4882-a69d-f1920225e478">IMFTranscodeSinkInfoProvider::GetSinkInfo</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

