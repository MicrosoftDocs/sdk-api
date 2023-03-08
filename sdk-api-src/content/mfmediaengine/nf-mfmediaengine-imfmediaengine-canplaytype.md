---
UID: NF:mfmediaengine.IMFMediaEngine.CanPlayType
title: IMFMediaEngine::CanPlayType (mfmediaengine.h)
description: Queries how likely it is that the Media Engine can play a specified type of media resource.
helpviewer_keywords: ["CanPlayType","CanPlayType method [Media Foundation]","CanPlayType method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","CanPlayType method","IMFMediaEngine.CanPlayType","IMFMediaEngine::CanPlayType","mf.imfmediaengine_canplaytype","mfmediaengine/IMFMediaEngine::CanPlayType"]
old-location: mf\imfmediaengine_canplaytype.htm
tech.root: mf
ms.assetid: 313F631F-7584-4F95-9208-B087CC12010E
ms.date: 12/05/2018
ms.keywords: CanPlayType, CanPlayType method [Media Foundation], CanPlayType method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],CanPlayType method, IMFMediaEngine.CanPlayType, IMFMediaEngine::CanPlayType, mf.imfmediaengine_canplaytype, mfmediaengine/IMFMediaEngine::CanPlayType
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngine::CanPlayType
 - mfmediaengine/IMFMediaEngine::CanPlayType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.CanPlayType
---

# IMFMediaEngine::CanPlayType


## -description

Queries how likely it is that the Media Engine can play a specified type of media resource.

## -parameters

### -param type [in]

A string that contains a MIME type with an optional codecs parameter, as defined in RFC 4281.

### -param pAnswer [out]

Receives an <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_canplay">MF_MEDIA_ENGINE_CANPLAY</a> enumeration value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>canPlayType</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The <b>canPlayType</b> attribute defines the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>"" (empty string)</td>
<td>The user-agent cannot play the resource, or the resource type is "application/octet-stream".</td>
</tr>
<tr>
<td>"probably"</td>
<td>The user-agent probably can play the resource.</td>
</tr>
<tr>
<td>"maybe"</td>
<td>Neither of the previous values applies.</td>
</tr>
</table>
 

The value "probably" is used because a MIME type for a media resource is generally not a complete description of the resource. For example, "video/mp4" specifies an MP4 file with video, but does not describe the codec. Even with the optional codecs parameter, the MIME type omits some information, such as the actual coded bit rate. Therefore, it is usually impossible to be certain that playback is possible until the actual media resource is opened.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>