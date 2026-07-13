---
UID: NF:mfobjects.IMFAudioMediaType.GetAudioFormat
title: IMFAudioMediaType::GetAudioFormat (mfobjects.h)
description: GetAudioFormat is no longer available for use as of Windows 7.
helpviewer_keywords: ["6a874e7b-9358-45e1-85be-7207bf46d93e","GetAudioFormat","GetAudioFormat method [Media Foundation]","GetAudioFormat method [Media Foundation]","IMFAudioMediaType interface","IMFAudioMediaType interface [Media Foundation]","GetAudioFormat method","IMFAudioMediaType.GetAudioFormat","IMFAudioMediaType::GetAudioFormat","mf.imfaudiomediatype_getaudioformat","mfobjects/IMFAudioMediaType::GetAudioFormat"]
old-location: mf\imfaudiomediatype_getaudioformat.htm
tech.root: mf
ms.assetid: 6a874e7b-9358-45e1-85be-7207bf46d93e
ms.date: 12/05/2018
ms.keywords: 6a874e7b-9358-45e1-85be-7207bf46d93e, GetAudioFormat, GetAudioFormat method [Media Foundation], GetAudioFormat method [Media Foundation],IMFAudioMediaType interface, IMFAudioMediaType interface [Media Foundation],GetAudioFormat method, IMFAudioMediaType.GetAudioFormat, IMFAudioMediaType::GetAudioFormat, mf.imfaudiomediatype_getaudioformat, mfobjects/IMFAudioMediaType::GetAudioFormat
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAudioMediaType::GetAudioFormat
 - mfobjects/IMFAudioMediaType::GetAudioFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioMediaType.GetAudioFormat
---

# IMFAudioMediaType::GetAudioFormat


## -description

<p class="CCE_Message">[<b>GetAudioFormat</b> is no longer available for use as of Windows 7. Instead, use the media type attributes to get the properties of the audio format.]

Returns a pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that describes the audio format.



## -returns

This method returns a pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

## -remarks

If you need to convert the media type into a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype">MFCreateWaveFormatExFromMFMediaType</a>.

There are no guarantees about how long the returned pointer is valid.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/audio-media-types">Audio Media Types</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype">IMFAudioMediaType</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>
