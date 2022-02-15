---
UID: NN:mfidl.IMFTranscodeProfile
title: IMFTranscodeProfile (mfidl.h)
description: Implemented by the transcode profile object.
helpviewer_keywords: ["IMFTranscodeProfile","IMFTranscodeProfile interface [Media Foundation]","IMFTranscodeProfile interface [Media Foundation]","described","mf.imftranscodeprofile","mfidl/IMFTranscodeProfile"]
old-location: mf\imftranscodeprofile.htm
tech.root: mf
ms.assetid: 82e012e0-84d8-4791-8b6f-bda58b498a90
ms.date: 12/05/2018
ms.keywords: IMFTranscodeProfile, IMFTranscodeProfile interface [Media Foundation], IMFTranscodeProfile interface [Media Foundation],described, mf.imftranscodeprofile, mfidl/IMFTranscodeProfile
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
 - IMFTranscodeProfile
 - mfidl/IMFTranscodeProfile
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
 - IMFTranscodeProfile
---

# IMFTranscodeProfile interface


## -description

Implemented by the transcode profile object.

The transcode profile stores configuration settings that the topology builder uses to generate the transcode topology for the output file. These configuration settings are specified by the caller and include audio and video stream properties, encoder settings, and  container settings that are specified by the caller.

To create the transcode profile object, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>. The configured transcode profile is passed to <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology">MFCreateTranscodeTopology</a>, which creates the transcode topology with the appropriate settings.

## -inheritance

The <b>IMFTranscodeProfile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTranscodeProfile</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/fast-transcode-objects">Fast Transcode Objects</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>
