---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.GetSinkInfo
title: IMFTranscodeSinkInfoProvider::GetSinkInfo (mfidl.h)
description: Gets the media types for the audio and video streams specified in the transcode profile.
helpviewer_keywords: ["GetSinkInfo","GetSinkInfo method [Media Foundation]","GetSinkInfo method [Media Foundation]","IMFTranscodeSinkInfoProvider interface","IMFTranscodeSinkInfoProvider interface [Media Foundation]","GetSinkInfo method","IMFTranscodeSinkInfoProvider.GetSinkInfo","IMFTranscodeSinkInfoProvider::GetSinkInfo","mf.imftranscodesinkinfoprovider_getsinkinfo","mfidl/IMFTranscodeSinkInfoProvider::GetSinkInfo"]
old-location: mf\imftranscodesinkinfoprovider_getsinkinfo.htm
tech.root: mf
ms.assetid: d880e13a-879e-4882-a69d-f1920225e478
ms.date: 12/05/2018
ms.keywords: GetSinkInfo, GetSinkInfo method [Media Foundation], GetSinkInfo method [Media Foundation],IMFTranscodeSinkInfoProvider interface, IMFTranscodeSinkInfoProvider interface [Media Foundation],GetSinkInfo method, IMFTranscodeSinkInfoProvider.GetSinkInfo, IMFTranscodeSinkInfoProvider::GetSinkInfo, mf.imftranscodesinkinfoprovider_getsinkinfo, mfidl/IMFTranscodeSinkInfoProvider::GetSinkInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTranscodeSinkInfoProvider::GetSinkInfo
 - mfidl/IMFTranscodeSinkInfoProvider::GetSinkInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTranscodeSinkInfoProvider.GetSinkInfo
---

# IMFTranscodeSinkInfoProvider::GetSinkInfo


## -description

Gets the media types for the audio and video streams specified in the transcode profile.

## -parameters

### -param pSinkInfo [out]

A pointer to an <a href="/windows/desktop/api/mfidl/ns-mfidl-mf_transcode_sink_info">MF_TRANSCODE_SINK_INFO</a> structure.

If the method succeeds, the method assigns <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> pointers to the <b>pAudioMediaType</b> and <b>pVideoMediaType</b> members of this structure. The method might set either member to <b>NULL</b>. If either member is non-NULL after the method returns, the caller must release the <b>IMFMediaType</b> pointers.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this method, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setprofile">IMFTranscodeSinkInfoProvider::SetProfile</a> to set the transcode profile. The <b>GetSinkInfo</b> method  uses the profile to create media types for the audio and video streams.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile Interface</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a>