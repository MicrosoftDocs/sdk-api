---
UID: NF:audioenginebaseapo.IAudioProcessingObject.IsOutputFormatSupported
title: IAudioProcessingObject::IsOutputFormatSupported (audioenginebaseapo.h)
description: The IsOutputFormatSupported method is used to verify that a specific output format is supported.
helpviewer_keywords: ["IAudioProcessingObject interface [Audio Devices]","IsOutputFormatSupported method","IAudioProcessingObject.IsOutputFormatSupported","IAudioProcessingObject::IsOutputFormatSupported","IsOutputFormatSupported","IsOutputFormatSupported method [Audio Devices]","IsOutputFormatSupported method [Audio Devices]","IAudioProcessingObject interface","audio.iaudioprocessingobject_isoutputformatsupported","audio_syseffects_r_542151d0-145f-4504-a282-e6473f1ae3c7.xml","audioenginebaseapo/IAudioProcessingObject::IsOutputFormatSupported"]
old-location: audio\iaudioprocessingobject_isoutputformatsupported.htm
tech.root: audio
ms.assetid: 19609332-9fc2-4a21-b947-f103a1cf2675
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObject interface [Audio Devices],IsOutputFormatSupported method, IAudioProcessingObject.IsOutputFormatSupported, IAudioProcessingObject::IsOutputFormatSupported, IsOutputFormatSupported, IsOutputFormatSupported method [Audio Devices], IsOutputFormatSupported method [Audio Devices],IAudioProcessingObject interface, audio.iaudioprocessingobject_isoutputformatsupported, audio_syseffects_r_542151d0-145f-4504-a282-e6473f1ae3c7.xml, audioenginebaseapo/IAudioProcessingObject::IsOutputFormatSupported
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
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
req.irql: All Levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObject::IsOutputFormatSupported
 - audioenginebaseapo/IAudioProcessingObject::IsOutputFormatSupported
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
 - IAudioProcessingObject.IsOutputFormatSupported
---

# IAudioProcessingObject::IsOutputFormatSupported


## -description

The <code>IsOutputFormatSupported</code> method is used to verify that a specific output format is supported.

## -parameters

### -param pOppositeFormat [in, optional]

A pointer to an IAudioMediaType interface. This parameter indicates the output format. This parameter must be set to <b>NULL</b> to indicate that the output format can be any type.

### -param pRequestedOutputFormat [in, optional]

A pointer to an <b>IAudioMediaType</b> interface. This parameter indicates the output format that is to be verified.

### -param ppSupportedOutputFormat [out, optional]

This parameter indicates the supported output format that is closest to the format to be verified.

## -returns

If the call completes successfully, the ppSupportedOutputFormat parameter returns a pRequestedOutputFormat pointer and the IsOutputFormatSupported method returns a value of S_OK. Otherwise, this method returns one of the following error codes:

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
The format of Input/output format pair is not supported. The ppSupportedOutPutFormat parameter returns a suggested new format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_FORMAT_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The format is not supported. The value of ppSupportedOutputFormat does not change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
An invalid pointer was passed to the function. The value of ppSupportedOutputFormat does not change.

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

There are differences in the implementation of the <code>IsOutputFormatSupported</code> method by the different APOs. For example, with certain implementations, the output can only be of type float when the input format is of type integer.

## -see-also

<a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a>



<a href="/windows/desktop/api/audioenginebaseapo/nn-audioenginebaseapo-iaudioprocessingobject">IAudioProcessingObject</a>