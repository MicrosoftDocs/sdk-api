---
UID: NF:mfidl.IMFTranscodeProfile.SetAudioAttributes
title: IMFTranscodeProfile::SetAudioAttributes (mfidl.h)
description: Sets audio stream configuration settings in the transcode profile.
helpviewer_keywords: ["IMFTranscodeProfile interface [Media Foundation]","SetAudioAttributes method","IMFTranscodeProfile.SetAudioAttributes","IMFTranscodeProfile::SetAudioAttributes","SetAudioAttributes","SetAudioAttributes method [Media Foundation]","SetAudioAttributes method [Media Foundation]","IMFTranscodeProfile interface","mf.imftranscodeprofile_setaudioattributes","mfidl/IMFTranscodeProfile::SetAudioAttributes"]
old-location: mf\imftranscodeprofile_setaudioattributes.htm
tech.root: mf
ms.assetid: 4118bb2b-8373-434a-896b-de5a1ba8c793
ms.date: 12/05/2018
ms.keywords: IMFTranscodeProfile interface [Media Foundation],SetAudioAttributes method, IMFTranscodeProfile.SetAudioAttributes, IMFTranscodeProfile::SetAudioAttributes, SetAudioAttributes, SetAudioAttributes method [Media Foundation], SetAudioAttributes method [Media Foundation],IMFTranscodeProfile interface, mf.imftranscodeprofile_setaudioattributes, mfidl/IMFTranscodeProfile::SetAudioAttributes
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
 - IMFTranscodeProfile::SetAudioAttributes
 - mfidl/IMFTranscodeProfile::SetAudioAttributes
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
 - IMFTranscodeProfile.SetAudioAttributes
---

# IMFTranscodeProfile::SetAudioAttributes


## -description

Sets audio stream configuration settings  in the transcode profile.

To get a list of compatible audio media types supported by the Media Foundation transform (MFT) encoder , call  <a href="/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes">MFTranscodeGetAudioOutputAvailableTypes</a>. You can get the attributes that are set on the required media type and set them on the transcode profile. To set the audio attributes properly, create a new attribute store and copy the attribute store from the required media media type by calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems">IMFAttributes::CopyAllItems</a>. This makes sure that the caller does not hold the references to the media type retrieved from the encoder. For example code, see <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>.

## -parameters

### -param pAttrs [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store that contains the configuration settings for the audio stream. The specified attribute values overwrite any existing values stored in the transcode profile. 

The following audio attributes can be set:

<ul>
<li>
<a href="/windows/desktop/medfound/audio-media-types">Audio Media Types</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-donot-insert-encoder">MF_TRANSCODE_DONOT_INSERT_ENCODER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-encodingprofile">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-qualityvsspeed">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
</ul>
To create the attribute store, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>. To set a specific attribute value in the attribute store, the caller must call the appropriate <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> methods depending on the data type of the attribute.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>