---
UID: NF:dmusics.IDirectMusicSynthSink.GetDesiredBufferSize
title: IDirectMusicSynthSink::GetDesiredBufferSize (dmusics.h)
description: The GetDesiredBufferSize method retrieves the synthesizer's preferred buffer size, expressed in samples.
helpviewer_keywords: ["GetDesiredBufferSize","GetDesiredBufferSize method [Audio Devices]","GetDesiredBufferSize method [Audio Devices]","IDirectMusicSynthSink interface","IDirectMusicSynthSink interface [Audio Devices]","GetDesiredBufferSize method","IDirectMusicSynthSink.GetDesiredBufferSize","IDirectMusicSynthSink::GetDesiredBufferSize","audio.idirectmusicsynthsink_getdesiredbuffersize","audmp-routines_be109f09-5ab8-46cd-925d-fe13d60c8ddb.xml","dmusics/IDirectMusicSynthSink::GetDesiredBufferSize"]
old-location: audio\idirectmusicsynthsink_getdesiredbuffersize.htm
tech.root: dshow
ms.assetid: a7c1892a-9aaf-4c53-a5df-6ce2b82d9d77
ms.date: 12/05/2018
ms.keywords: GetDesiredBufferSize, GetDesiredBufferSize method [Audio Devices], GetDesiredBufferSize method [Audio Devices],IDirectMusicSynthSink interface, IDirectMusicSynthSink interface [Audio Devices],GetDesiredBufferSize method, IDirectMusicSynthSink.GetDesiredBufferSize, IDirectMusicSynthSink::GetDesiredBufferSize, audio.idirectmusicsynthsink_getdesiredbuffersize, audmp-routines_be109f09-5ab8-46cd-925d-fe13d60c8ddb.xml, dmusics/IDirectMusicSynthSink::GetDesiredBufferSize
req.header: dmusics.h
req.include-header: Dmusics.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectMusicSynthSink::GetDesiredBufferSize
 - dmusics/IDirectMusicSynthSink::GetDesiredBufferSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynthSink.GetDesiredBufferSize
archived: true
---

# IDirectMusicSynthSink::GetDesiredBufferSize


## -description

The <code>GetDesiredBufferSize</code> method retrieves the synthesizer's preferred buffer size, expressed in samples.

## -parameters

### -param pdwBufferSizeInSamples

Output pointer for the buffer size. This parameter points to a caller-allocated variable into which the method writes the desired buffer length, expressed in samples.

## -returns

<code>GetDesiredBufferSize</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not set.

</td>
</tr>
</table>

## -remarks

The <code>GetDesiredBufferSize</code> method returns the desired buffer size based on the current format of the synth. DirectSound buffers passed to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setdirectsound">IDirectMusicSynthSink::SetDirectSound</a> might be invalid unless they are at least this size.

For more information, see the description of the <b>IDirectMusicPort</b> interface in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setdirectsound">IDirectMusicSynthSink::SetDirectSound</a>