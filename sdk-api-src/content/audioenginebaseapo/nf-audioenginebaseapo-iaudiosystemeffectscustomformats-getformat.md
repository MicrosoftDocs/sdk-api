---
UID: NF:audioenginebaseapo.IAudioSystemEffectsCustomFormats.GetFormat
title: IAudioSystemEffectsCustomFormats::GetFormat (audioenginebaseapo.h)
description: The GetFormat method retrieves an IAudioMediaType representation of a custom format.
helpviewer_keywords: ["GetFormat","GetFormat method [Audio Devices]","GetFormat method [Audio Devices]","IAudioSystemEffectsCustomFormats interface","IAudioSystemEffectsCustomFormats interface [Audio Devices]","GetFormat method","IAudioSystemEffectsCustomFormats.GetFormat","IAudioSystemEffectsCustomFormats::GetFormat","audio.iaudiosystemeffectscustomformats_getformat","audio_syseffects_r_6d606a4f-7fce-4ae6-af5b-77a3baf2e41e.xml","audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormat"]
old-location: audio\iaudiosystemeffectscustomformats_getformat.htm
tech.root: audio
ms.assetid: 0eab885f-32f7-47d3-b9b1-684eb3d2cd37
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [Audio Devices], GetFormat method [Audio Devices],IAudioSystemEffectsCustomFormats interface, IAudioSystemEffectsCustomFormats interface [Audio Devices],GetFormat method, IAudioSystemEffectsCustomFormats.GetFormat, IAudioSystemEffectsCustomFormats::GetFormat, audio.iaudiosystemeffectscustomformats_getformat, audio_syseffects_r_6d606a4f-7fce-4ae6-af5b-77a3baf2e41e.xml, audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormat
req.header: audioenginebaseapo.h
req.include-header: Audioenginebaseapo.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
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
req.irql: All levels.
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioSystemEffectsCustomFormats::GetFormat
 - audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioSystemEffectsCustomFormats.GetFormat
---

# IAudioSystemEffectsCustomFormats::GetFormat


## -description

The <code>GetFormat</code> method retrieves an <a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a> representation of a custom format.

## -parameters

### -param nFormat [in]

Specifies the index of a supported format. This parameter can be any value in the range from zero to one less than the return value of <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformatcount">GetFormatCount</a>. In other words, any value in the range from zero to GetFormatCount( ) - 1.

### -param ppFormat [out, optional]

Specifies a pointer to a pointer to an <b>IAudioMediaType</b> interface. It is the responsibility of the caller to release the <b>IAudioMediaType</b> interface to which the <i>ppFormat</i> parameter points.

## -returns

The <code>GetFormat</code> method returns S_OK when the call is successful. Otherwise, it returns one of the error codes shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer passed to function

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Return buffer cannot be allocated

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
nFormat is out of range

</td>
</tr>
</table>

## -remarks

When the audio system calls the <code>GetFormat</code> method, the sAPO creates an audio media type object and returns an <b>IAudioMediaType</b> interface. The sAPO implementation can use the <a href="/windows/desktop/api/audiomediatype/nf-audiomediatype-createaudiomediatype">CreateAudioMediaType</a> utility function to create the audio media type object.

## -see-also

<a href="/windows/desktop/api/audiomediatype/nf-audiomediatype-createaudiomediatype">CreateAudioMediaType</a>



<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformatcount">GetFormatCount</a>



<a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a>