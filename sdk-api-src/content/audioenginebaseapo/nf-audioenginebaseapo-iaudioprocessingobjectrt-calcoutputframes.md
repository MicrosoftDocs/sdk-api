---
UID: NF:audioenginebaseapo.IAudioProcessingObjectRT.CalcOutputFrames
title: IAudioProcessingObjectRT::CalcOutputFrames (audioenginebaseapo.h)
description: The CalcOutputFrames method returns the number of output frames that an APO requires for a given number of input frames.
helpviewer_keywords: ["CalcOutputFrames","CalcOutputFrames method [Audio Devices]","CalcOutputFrames method [Audio Devices]","IAudioProcessingObjectRT interface","IAudioProcessingObjectRT interface [Audio Devices]","CalcOutputFrames method","IAudioProcessingObjectRT.CalcOutputFrames","IAudioProcessingObjectRT::CalcOutputFrames","audio.iaudioprocessingobjectrt_calcoutputframes","audio_syseffects_r_1352a553-5788-46cb-be25-1d3d8e6ab963.xml","audioenginebaseapo/IAudioProcessingObjectRT::CalcOutputFrames"]
old-location: audio\iaudioprocessingobjectrt_calcoutputframes.htm
tech.root: audio
ms.assetid: af558f8c-a38e-44d0-ad50-5e650f86cf2e
ms.date: 12/05/2018
ms.keywords: CalcOutputFrames, CalcOutputFrames method [Audio Devices], CalcOutputFrames method [Audio Devices],IAudioProcessingObjectRT interface, IAudioProcessingObjectRT interface [Audio Devices],CalcOutputFrames method, IAudioProcessingObjectRT.CalcOutputFrames, IAudioProcessingObjectRT::CalcOutputFrames, audio.iaudioprocessingobjectrt_calcoutputframes, audio_syseffects_r_1352a553-5788-46cb-be25-1d3d8e6ab963.xml, audioenginebaseapo/IAudioProcessingObjectRT::CalcOutputFrames
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
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObjectRT::CalcOutputFrames
 - audioenginebaseapo/IAudioProcessingObjectRT::CalcOutputFrames
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
 - IAudioProcessingObjectRT.CalcOutputFrames
---

# IAudioProcessingObjectRT::CalcOutputFrames


## -description

The <code>CalcOutputFrames</code> method returns the number of output frames that an APO requires for a given number of input frames.

## -parameters

### -param u32InputFrameCount [in]

This is a count of the number of input frames.

## -returns

The <code>CalcOutputFrames</code> method returns the number of output frames that an APO will generate for a given number of input frames.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
</table>

## -remarks

The <code>CalcOutputFrames</code> method can be called form a real-time processing thread. The implementation of this method must not block or touch paged memory and it should not call any system blocking routines.

