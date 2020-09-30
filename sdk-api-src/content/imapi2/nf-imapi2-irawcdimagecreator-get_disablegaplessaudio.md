---
UID: NF:imapi2.IRawCDImageCreator.get_DisableGaplessAudio
title: IRawCDImageCreator::get_DisableGaplessAudio (imapi2.h)
description: Retrieves the current value that specifies if &quot;Gapless Audio&quot; recording is disabled. This property defaults to a value of VARIANT_FALSE, which disables the use of &quot;gapless&quot; recording between consecutive audio tracks.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_DisableGaplessAudio method","IRawCDImageCreator.get_DisableGaplessAudio","IRawCDImageCreator::get_DisableGaplessAudio","get_DisableGaplessAudio","get_DisableGaplessAudio method [IMAPI]","get_DisableGaplessAudio method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_disablegaplessaudio","imapi2/IRawCDImageCreator::get_DisableGaplessAudio"]
old-location: imapi\irawcdimagecreator_get_disablegaplessaudio.htm
tech.root: imapi
ms.assetid: 5f3bf774-3e09-40e9-bc0b-f33bfd046a51
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_DisableGaplessAudio method, IRawCDImageCreator.get_DisableGaplessAudio, IRawCDImageCreator::get_DisableGaplessAudio, get_DisableGaplessAudio, get_DisableGaplessAudio method [IMAPI], get_DisableGaplessAudio method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_disablegaplessaudio, imapi2/IRawCDImageCreator::get_DisableGaplessAudio
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IRawCDImageCreator::get_DisableGaplessAudio
 - imapi2/IRawCDImageCreator::get_DisableGaplessAudio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageCreator.get_DisableGaplessAudio
---

# IRawCDImageCreator::get_DisableGaplessAudio


## -description

Retrieves the current value that specifies if "Gapless Audio" recording is disabled. This property defaults to a value of  <b>VARIANT_FALSE</b>, which disables the use of "gapless" recording between consecutive audio tracks.

## -parameters

### -param value [out]

A <b>VARIANT_BOOL</b> value that specifies if "Gapless Audio" is disabled. A value of <b>VARIANT_FALSE</b> indicates that "Gapless Audio" is disabled; <b>VARIANT_TRUE</b> indicates that it is enabled.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

When disabled, by default, the audio tracks will have the standard 2-second (150 sector) silent gap between tracks.  When enabled, the last 2  seconds of audio data from the previous audio track are encoded in the pregap area of the next audio track, enabling seamless transitions between tracks.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_disablegaplessaudio">IRawCDImageCreator::put_DisableGaplessAudio</a>