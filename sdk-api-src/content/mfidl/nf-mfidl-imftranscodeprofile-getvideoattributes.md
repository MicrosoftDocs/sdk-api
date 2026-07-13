---
UID: NF:mfidl.IMFTranscodeProfile.GetVideoAttributes
title: IMFTranscodeProfile::GetVideoAttributes (mfidl.h)
description: Gets the video stream settings that are currently set in the transcode profile.
helpviewer_keywords: ["GetVideoAttributes","GetVideoAttributes method [Media Foundation]","GetVideoAttributes method [Media Foundation]","IMFTranscodeProfile interface","IMFTranscodeProfile interface [Media Foundation]","GetVideoAttributes method","IMFTranscodeProfile.GetVideoAttributes","IMFTranscodeProfile::GetVideoAttributes","mf.imftranscodeprofile_getvideoattributes","mfidl/IMFTranscodeProfile::GetVideoAttributes"]
old-location: mf\imftranscodeprofile_getvideoattributes.htm
tech.root: mf
ms.assetid: 734cb4d0-7017-4a30-9d0c-a6b5ce42fec6
ms.date: 12/05/2018
ms.keywords: GetVideoAttributes, GetVideoAttributes method [Media Foundation], GetVideoAttributes method [Media Foundation],IMFTranscodeProfile interface, IMFTranscodeProfile interface [Media Foundation],GetVideoAttributes method, IMFTranscodeProfile.GetVideoAttributes, IMFTranscodeProfile::GetVideoAttributes, mf.imftranscodeprofile_getvideoattributes, mfidl/IMFTranscodeProfile::GetVideoAttributes
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
 - IMFTranscodeProfile::GetVideoAttributes
 - mfidl/IMFTranscodeProfile::GetVideoAttributes
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
 - IMFTranscodeProfile.GetVideoAttributes
---

# IMFTranscodeProfile::GetVideoAttributes


## -description

Gets the video stream settings that are currently set in the transcode profile.

## -parameters

### -param ppAttrs [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store containing the current video stream settings. Caller must release the interface pointer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If there are no container attributes set in the transcode profile, the <b>GetVideoAttributes</b> method  succeeds and  <i>ppAttrs</i> receives <b>NULL</b>.

To get a specific attribute value, the caller must call the appropriate <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> method depending on the data type of the attribute, and specify the attribute name. The following list shows the video attributes:

<ul>
<li>
<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-encodingprofile">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-qualityvsspeed">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-donot-insert-encoder">MF_TRANSCODE_DONOT_INSERT_ENCODER</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>