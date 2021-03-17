---
UID: NF:audioenginebaseapo.IAudioProcessingObjectRT.CalcInputFrames
title: IAudioProcessingObjectRT::CalcInputFrames (audioenginebaseapo.h)
description: The CalcInputFrames method returns the number of input frames that an APO requires to generate a given number of output frames.
helpviewer_keywords: ["CalcInputFrames","CalcInputFrames method [Audio Devices]","CalcInputFrames method [Audio Devices]","IAudioProcessingObjectRT interface","IAudioProcessingObjectRT interface [Audio Devices]","CalcInputFrames method","IAudioProcessingObjectRT.CalcInputFrames","IAudioProcessingObjectRT::CalcInputFrames","audio.iaudioprocessingobjectrt_calcinputframes","audio_syseffects_r_e44e803b-e1cf-40d1-b4d1-39e765a5a694.xml","audioenginebaseapo/IAudioProcessingObjectRT::CalcInputFrames"]
old-location: audio\iaudioprocessingobjectrt_calcinputframes.htm
tech.root: audio
ms.assetid: cadebe77-5c2e-4702-9bc9-5ed0ea255722
ms.date: 12/05/2018
ms.keywords: CalcInputFrames, CalcInputFrames method [Audio Devices], CalcInputFrames method [Audio Devices],IAudioProcessingObjectRT interface, IAudioProcessingObjectRT interface [Audio Devices],CalcInputFrames method, IAudioProcessingObjectRT.CalcInputFrames, IAudioProcessingObjectRT::CalcInputFrames, audio.iaudioprocessingobjectrt_calcinputframes, audio_syseffects_r_e44e803b-e1cf-40d1-b4d1-39e765a5a694.xml, audioenginebaseapo/IAudioProcessingObjectRT::CalcInputFrames
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
 - IAudioProcessingObjectRT::CalcInputFrames
 - audioenginebaseapo/IAudioProcessingObjectRT::CalcInputFrames
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
 - IAudioProcessingObjectRT.CalcInputFrames
---

# IAudioProcessingObjectRT::CalcInputFrames


## -description

The <code>CalcInputFrames</code> method returns the number of input frames that an APO requires to generate a given number of output frames.

## -parameters

### -param u32OutputFrameCount

This is a count of the number of output frames.

## -returns

The <code>CalcInputFrames</code> method returns the number of input frames that are required to generate the given number of output frames.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
</table>

## -remarks

The <code>CalcInputFrames</code> method is called from a real-time processing thread. The implementation of this method must not touch paged memory and it should not call any system blocking routines.

