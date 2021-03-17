---
UID: NF:imapi2.IRawCDImageCreator.put_DisableGaplessAudio
title: IRawCDImageCreator::put_DisableGaplessAudio (imapi2.h)
description: Sets the value that specifies if &quot;Gapless Audio&quot; recording is disabled. This property defaults to a value of VARIANT_FALSE, which disables the use of &quot;gapless&quot; recording between consecutive audio tracks.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","put_DisableGaplessAudio method","IRawCDImageCreator.put_DisableGaplessAudio","IRawCDImageCreator::put_DisableGaplessAudio","imapi.irawcdimagecreator_put_disablegaplessaudio","imapi2/IRawCDImageCreator::put_DisableGaplessAudio","put_DisableGaplessAudio","put_DisableGaplessAudio method [IMAPI]","put_DisableGaplessAudio method [IMAPI]","IRawCDImageCreator interface"]
old-location: imapi\irawcdimagecreator_put_disablegaplessaudio.htm
tech.root: imapi
ms.assetid: c9e17ed7-f51a-4b28-82db-36cad1aedd39
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],put_DisableGaplessAudio method, IRawCDImageCreator.put_DisableGaplessAudio, IRawCDImageCreator::put_DisableGaplessAudio, imapi.irawcdimagecreator_put_disablegaplessaudio, imapi2/IRawCDImageCreator::put_DisableGaplessAudio, put_DisableGaplessAudio, put_DisableGaplessAudio method [IMAPI], put_DisableGaplessAudio method [IMAPI],IRawCDImageCreator interface
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
 - IRawCDImageCreator::put_DisableGaplessAudio
 - imapi2/IRawCDImageCreator::put_DisableGaplessAudio
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
 - IRawCDImageCreator.put_DisableGaplessAudio
---

# IRawCDImageCreator::put_DisableGaplessAudio


## -description

Sets the value that specifies if "Gapless Audio" recording is disabled. This property defaults to a value of  <b>VARIANT_FALSE</b>, which disables the use of "gapless" recording between consecutive audio tracks.

## -parameters

### -param value

A <b>VARIANT_BOOL</b> value that specifies if "Gapless Audio" is disabled. Setting a value of <b>VARIANT_FALSE</b> disables "Gapless Audio", while <b>VARIANT_TRUE</b> enables it.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

When disabled, by default, the audio tracks will have the standard 2-second (150 sector) silent gap between tracks.  When enabled, the last 2  seconds of audio data from the previous audio track are encoded in the pregap area of the next audio track, enabling seamless transitions between tracks.

It is recommended that this property value is only set before the process of adding tracks to the image has begun as any changes afterwards could result in adverse effects to other image properties.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_disablegaplessaudio">IRawCDImageCreator::get_DisableGaplessAudio</a>