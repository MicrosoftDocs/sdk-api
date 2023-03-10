---
UID: NF:mfidl.MFCreateTranscodeTopology
title: MFCreateTranscodeTopology function (mfidl.h)
description: Creates a partial transcode topology.
helpviewer_keywords: ["MFCreateTranscodeTopology","MFCreateTranscodeTopology function [Media Foundation]","mf.mfcreatetranscodetopology","mfidl/MFCreateTranscodeTopology"]
old-location: mf\mfcreatetranscodetopology.htm
tech.root: mf
ms.assetid: ef3f19bf-1db9-459d-9617-d6cca9d6aba7
ms.date: 12/05/2018
ms.keywords: MFCreateTranscodeTopology, MFCreateTranscodeTopology function [Media Foundation], mf.mfcreatetranscodetopology, mfidl/MFCreateTranscodeTopology
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateTranscodeTopology
 - mfidl/MFCreateTranscodeTopology
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateTranscodeTopology
---

# MFCreateTranscodeTopology function


## -description

Creates a partial transcode topology.

The underlying topology builder creates a partial topology by connecting the required pipeline objects:
source, encoder, and sink. The encoder and the sink are configured according to the settings specified by the caller in the transcode profile. 

To create the transcode profile object, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a> function and set the required attributes by calling the appropriate the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> methods. 

The configured transcode profile is passed to the <b>MFCreateTranscodeTopology</b> function, which creates the transcode topology with the appropriate settings. The caller can then set this topology on the Media Session and start the session to begin the encoding process. When the Media Session ends, the transcoded file is generated.

## -parameters

### -param pSrc [in]

A pointer to a media source that encapsulates the source file to be transcoded. The media source object exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface and can be created by using the source resolver. For more information, see <a href="/windows/desktop/medfound/using-the-source-resolver">Using the Source Resolver</a>.

### -param pwszOutputFilePath [in]

A pointer to a null-terminated string that contains the name and path of the output file to be generated.

### -param pProfile [in]

A pointer to the transcode profile that contains the configuration settings for the audio stream, the video stream, and the container to which the file is written. The transcode profile object exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> interface and must be created by calling the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a> function. After the object has been created the caller must provide the configuration settings by calling appropriate the <b>IMFTranscodeProfile</b> methods.

### -param ppTranscodeTopo [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the transcode topology object. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function call succeeded, and <i>ppTranscodeTopo</i> receives a pointer to the transcode topology.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszOutputFilePath</i> contains invalid characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_MEDIA_SOURCE_NO_STREAMS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
No streams are selected in the media source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_NO_CONTAINERTYPE</b></dt>
</dl>
</td>
<td width="60%">
The profile does not contain the <a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a> attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_NO_MATCHING_ENCODER</b></dt>
</dl>
</td>
<td width="60%">
For one or more streams, cannot find an encoder that accepts the media type given in the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_PROFILE_NO_MATCHING_STREAMS</b></dt>
</dl>
</td>
<td width="60%">
The profile does not specify a media type for any of the selected streams on the media source.

</td>
</tr>
</table>

## -remarks

For example code that uses this function, see the following topics:

<ul>
<li>
<a href="/windows/desktop/medfound/tutorial--encoding-an-mp4-file-">Tutorial: Encoding an MP4 File</a>
</li>
<li>
<a href="/windows/desktop/medfound/tutorial--converting-an-mp3-file-to-a-wma-file">Tutorial: Encoding a WMA File</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>