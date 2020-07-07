---
UID: NN:mfidl.IMFTranscodeProfile
title: IMFTranscodeProfile (mfidl.h)
description: Implemented by the transcode profile object.
helpviewer_keywords: ["IMFTranscodeProfile","IMFTranscodeProfile interface [Media Foundation]","IMFTranscodeProfile interface [Media Foundation]","described","mf.imftranscodeprofile","mfidl/IMFTranscodeProfile"]
old-location: mf\imftranscodeprofile.htm
tech.root: medfound
ms.assetid: 82e012e0-84d8-4791-8b6f-bda58b498a90
ms.date: 12/05/2018
ms.keywords: IMFTranscodeProfile, IMFTranscodeProfile interface [Media Foundation], IMFTranscodeProfile interface [Media Foundation],described, mf.imftranscodeprofile, mfidl/IMFTranscodeProfile
f1_keywords:
- mfidl/IMFTranscodeProfile
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
- IMFTranscodeProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTranscodeProfile interface


## -description


Implemented by the transcode profile object.

The transcode profile stores configuration settings that the topology builder uses to generate the transcode topology for the output file. These configuration settings are specified by the caller and include audio and video stream properties, encoder settings, and  container settings that are specified by the caller.

To create the transcode profile object, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>. The configured transcode profile is passed to <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology">MFCreateTranscodeTopology</a>, which creates the transcode topology with the appropriate settings. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTranscodeProfile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTranscodeProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTranscodeProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes">GetAudioAttributes</a>
</td>
<td align="left" width="63%">
Gets the audio stream settings that are currently set in the transcode profile.
  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes">GetContainerAttributes</a>
</td>
<td align="left" width="63%">
Gets the container settings that are currently set in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes">GetVideoAttributes</a>
</td>
<td align="left" width="63%">
Gets the video stream settings that are currently set in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes">SetAudioAttributes</a>
</td>
<td align="left" width="63%">
Sets audio stream configuration settings  in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes">SetContainerAttributes</a>
</td>
<td align="left" width="63%">
Sets container configuration settings  in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes">SetVideoAttributes</a>
</td>
<td align="left" width="63%">
Sets video stream configuration settings  in the transcode profile. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/fast-transcode-objects">Fast Transcode Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/transcode-api">Transcode API</a>
 

 

