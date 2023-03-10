---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.SetProfile
title: IMFTranscodeSinkInfoProvider::SetProfile (mfidl.h)
description: Sets the transcoding profile on the transcode sink activation object.
helpviewer_keywords: ["IMFTranscodeSinkInfoProvider interface [Media Foundation]","SetProfile method","IMFTranscodeSinkInfoProvider.SetProfile","IMFTranscodeSinkInfoProvider::SetProfile","SetProfile","SetProfile method [Media Foundation]","SetProfile method [Media Foundation]","IMFTranscodeSinkInfoProvider interface","mf.imftranscodesinkinfoprovider_setprofile","mfidl/IMFTranscodeSinkInfoProvider::SetProfile"]
old-location: mf\imftranscodesinkinfoprovider_setprofile.htm
tech.root: mf
ms.assetid: 81137d8c-70b2-4a0a-a1b4-16a2f50f134b
ms.date: 12/05/2018
ms.keywords: IMFTranscodeSinkInfoProvider interface [Media Foundation],SetProfile method, IMFTranscodeSinkInfoProvider.SetProfile, IMFTranscodeSinkInfoProvider::SetProfile, SetProfile, SetProfile method [Media Foundation], SetProfile method [Media Foundation],IMFTranscodeSinkInfoProvider interface, mf.imftranscodesinkinfoprovider_setprofile, mfidl/IMFTranscodeSinkInfoProvider::SetProfile
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
 - IMFTranscodeSinkInfoProvider::SetProfile
 - mfidl/IMFTranscodeSinkInfoProvider::SetProfile
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
 - IMFTranscodeSinkInfoProvider.SetProfile
---

# IMFTranscodeSinkInfoProvider::SetProfile


## -description

Sets the transcoding profile on the transcode sink activation object.

## -parameters

### -param pProfile [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> interface. To get a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this method, initialize the profile object as follows:

<ul>
<li>Set the <a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a> attribute to specify the container type of the output file.</li>
<li>If the output file will have a video stream, set video attributes by calling the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes">IMFTranscodeProfile::SetVideoAttributes</a> method.</li>
<li>If the output file will have an audio stream, set audio attributes by calling the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes">IMFTranscodeProfile::SetAudioAttributes</a> method.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a>