---
UID: NS:mfidl._MF_TRANSCODE_SINK_INFO
title: MF_TRANSCODE_SINK_INFO (mfidl.h)
author: windows-sdk-content
description: Contains information about the audio and video streams for the transcode sink activation object.
old-location: mf\mf_transcode_sink_info.htm
tech.root: medfound
ms.assetid: b8f66128-88d5-4fe0-99f3-59621080be5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MF_TRANSCODE_SINK_INFO, MF_TRANSCODE_SINK_INFO structure [Media Foundation], mf.mf_transcode_sink_info, mfidl/MF_TRANSCODE_SINK_INFO
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
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
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_TRANSCODE_SINK_INFO
product: Windows
targetos: Windows
req.typenames: MF_TRANSCODE_SINK_INFO
req.redist: 
ms.custom: 19H1
---

# MF_TRANSCODE_SINK_INFO structure


## -description


Contains information about the audio and video streams for the transcode sink activation object.

To get the information stored in this structure, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-getsinkinfo">IMFTranscodeSinkInfoProvider::GetSinkInfo</a>.


## -struct-fields




### -field dwVideoStreamID

The stream identifier of the video stream.


### -field pVideoMediaType

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type for the  video stream. This member can be <b>NULL</b>.


### -field dwAudioStreamID

The stream identifier of the audio stream.


### -field pAudioMediaType

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type for the  audio stream. This member can be <b>NULL</b>.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-getsinkinfo">IMFTranscodeSinkInfoProvider::GetSinkInfo</a> method assigns <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> pointers to the <b>pAudioMediaType</b> and <b>pVideoMediaType</b> members of this structure. The method might set either member to <b>NULL</b>. If either member is non-<b>NULL</b> after the method returns, the caller must release the <b>IMFMediaType</b> pointers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-getsinkinfo">IMFTranscodeSinkInfoProvider::GetSinkInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

