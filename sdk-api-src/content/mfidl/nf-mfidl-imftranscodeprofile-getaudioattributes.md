---
UID: NF:mfidl.IMFTranscodeProfile.GetAudioAttributes
title: IMFTranscodeProfile::GetAudioAttributes (mfidl.h)
description: Gets the audio stream settings that are currently set in the transcode profile.
helpviewer_keywords: ["GetAudioAttributes","GetAudioAttributes method [Media Foundation]","GetAudioAttributes method [Media Foundation]","IMFTranscodeProfile interface","IMFTranscodeProfile interface [Media Foundation]","GetAudioAttributes method","IMFTranscodeProfile.GetAudioAttributes","IMFTranscodeProfile::GetAudioAttributes","mf.imftranscodeprofile_getaudioattributes","mfidl/IMFTranscodeProfile::GetAudioAttributes"]
old-location: mf\imftranscodeprofile_getaudioattributes.htm
tech.root: mf
ms.assetid: c02dabfe-33ef-4835-a707-d1350b18629f
ms.date: 12/05/2018
ms.keywords: GetAudioAttributes, GetAudioAttributes method [Media Foundation], GetAudioAttributes method [Media Foundation],IMFTranscodeProfile interface, IMFTranscodeProfile interface [Media Foundation],GetAudioAttributes method, IMFTranscodeProfile.GetAudioAttributes, IMFTranscodeProfile::GetAudioAttributes, mf.imftranscodeprofile_getaudioattributes, mfidl/IMFTranscodeProfile::GetAudioAttributes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTranscodeProfile::GetAudioAttributes
 - mfidl/IMFTranscodeProfile::GetAudioAttributes
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
 - IMFTranscodeProfile.GetAudioAttributes
---

# IMFTranscodeProfile::GetAudioAttributes


## -description

Gets the audio stream settings that are currently set in the transcode profile.

## -parameters

### -param ppAttrs [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store containing the current audio stream settings. Caller must release the interface pointer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If there are no audio attributes set in the transcode profile, the call to <b>GetAudioAttributes</b> succeeds and  <i>ppAttrs</i> receives <b>NULL</b>.

To get a specific attribute value, the caller must call the appropriate <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> method depending on the data type of the attribute, and specify the attribute name. The following topics describe the audio attributes:

<ul>
<li>
<a href="/windows/desktop/medfound/audio-media-types">Audio Media Types</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-encodingprofile">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-qualityvsspeed">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>