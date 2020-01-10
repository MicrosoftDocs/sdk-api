---
UID: NF:mfidl.IMFTranscodeProfile.SetVideoAttributes
title: IMFTranscodeProfile::SetVideoAttributes (mfidl.h)
description: Sets video stream configuration settings in the transcode profile.
old-location: mf\imftranscodeprofile_setvideoattributes.htm
tech.root: medfound
ms.assetid: e68653c5-5663-4839-a482-2244e147f4b9
ms.date: 12/05/2018
ms.keywords: IMFTranscodeProfile interface [Media Foundation],SetVideoAttributes method, IMFTranscodeProfile.SetVideoAttributes, IMFTranscodeProfile::SetVideoAttributes, SetVideoAttributes, SetVideoAttributes method [Media Foundation], SetVideoAttributes method [Media Foundation],IMFTranscodeProfile interface, mf.imftranscodeprofile_setvideoattributes, mfidl/IMFTranscodeProfile::SetVideoAttributes
f1_keywords:
- mfidl/IMFTranscodeProfile.SetVideoAttributes
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfidl.h
api_name:
- IMFTranscodeProfile.SetVideoAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTranscodeProfile::SetVideoAttributes


## -description


Sets video stream configuration settings  in the transcode profile.

 For example code, see <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>.


## -parameters




### -param pAttrs [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store that contains contains the configuration settings for the video stream. The specified attribute values overwrites any existing values stored in the transcode profile. 

The following video attributes can be set:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/video-media-types">Video Media Types</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-donot-insert-encoder">MF_TRANSCODE_DONOT_INSERT_ENCODER</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-encodingprofile">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-qualityvsspeed">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
</ul>
To create the attribute store, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>. To set a specific attribute value in the attribute store, the caller must call the appropriate <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> methods depending on the data type of the attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/transcode-api">Transcode API</a>
 

 

