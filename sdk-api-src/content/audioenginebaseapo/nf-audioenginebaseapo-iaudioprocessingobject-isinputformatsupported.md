---
UID: NF:audioenginebaseapo.IAudioProcessingObject.IsInputFormatSupported
title: IAudioProcessingObject::IsInputFormatSupported (audioenginebaseapo.h)
description: This method negotiates with the Windows Vista audio engine to establish a data format for the stream of audio data.
helpviewer_keywords: ["IAudioProcessingObject interface [Audio Devices]","IsInputFormatSupported method","IAudioProcessingObject.IsInputFormatSupported","IAudioProcessingObject::IsInputFormatSupported","IsInputFormatSupported","IsInputFormatSupported method [Audio Devices]","IsInputFormatSupported method [Audio Devices]","IAudioProcessingObject interface","audio.iaudioprocessingobject_isinputformatsupported","audio_syseffects_r_d9f38647-9d9e-4776-98d4-1a9904271dc1.xml","audioenginebaseapo/IAudioProcessingObject::IsInputFormatSupported"]
old-location: audio\iaudioprocessingobject_isinputformatsupported.htm
tech.root: audio
ms.assetid: 11eebb5d-21fd-48f7-8929-cd2612a3f451
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObject interface [Audio Devices],IsInputFormatSupported method, IAudioProcessingObject.IsInputFormatSupported, IAudioProcessingObject::IsInputFormatSupported, IsInputFormatSupported, IsInputFormatSupported method [Audio Devices], IsInputFormatSupported method [Audio Devices],IAudioProcessingObject interface, audio.iaudioprocessingobject_isinputformatsupported, audio_syseffects_r_d9f38647-9d9e-4776-98d4-1a9904271dc1.xml, audioenginebaseapo/IAudioProcessingObject::IsInputFormatSupported
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later Windows operating systems.
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
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObject::IsInputFormatSupported
 - audioenginebaseapo/IAudioProcessingObject::IsInputFormatSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioenginebaseapo.idl
 - Audioenginebaseapo.idl.dll
api_name:
 - IAudioProcessingObject.IsInputFormatSupported
---

# IAudioProcessingObject::IsInputFormatSupported


## -description

This method negotiates with the Windows Vista audio engine to establish a data format for the stream of audio data.

## -parameters

### -param pOppositeFormat [in, optional]

A pointer to an <a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a> interface. This parameter is used to indicate the output format of the data. The value of pOppositeFormat must be set to <b>NULL</b> to indicate that the output format can be any type.

### -param pRequestedInputFormat [in, optional]

A pointer to an <a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a> interface. This parameter is used to indicate the input format that is to be verified.

### -param ppSupportedInputFormat [out, optional]

This parameter indicates the supported format that is closest to the format to be verified.

## -returns

If the call completed successfully, the ppSupportedInputFormat parameter returns a pRequestedInputFormat pointer and the IsInputFormatSupported method returns a value of S_OK. Otherwise, this method returns one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The format of the input/output format pair is not supported. ppSupportedInputFormat returns a suggested new format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_FORMAT_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The format to be verified is not supported. The value of ppSupportedInputFormat does not change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer that is passed to the method. The value of ppSupportedInputFormat does not change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other HRESULT values</b></dt>
</dl>
</td>
<td width="60%">
These additional error conditions are tracked by the audio engine.

</td>
</tr>
</table>

## -remarks

There are differences in the implementation of the <code>IsInputFormatSupported</code> method by the different APOs. For example, with certain implementations, the output can only be of type float when the input format is of type integer.

To initiate format negotiation, the audio service first sets the output of the LFX sAPO to the default float32-based format. The audio service then calls the <code>IAudioProcessingObject::IsInputFormatSupported</code> method of the LFX sAPO, suggests the default format, and monitors the HRESULT response of this method. If the input of the LFX sAPO can support the suggested format, it returns S_OK, together with a reference to the supported format. If the input of the LFX sAPO cannot support the suggested format, it returns S_FALSE together with a reference to a format that is the closest match to the suggested one. If the LFX sAPO cannot support the suggested format and does not have a close match, it returns APOERR_FORMAT_NOT_SUPPORTED. The GFX sAPO works with the output format of the LFX sAPO. So the GFX sAPO is not involved in the format negotiation process.