---
UID: NF:audioenginebaseapo.IAudioProcessingObjectRT.CalcOutputFrames
title: IAudioProcessingObjectRT::CalcOutputFrames
author: windows-sdk-content
description: The CalcOutputFrames method returns the number of output frames that an APO requires for a given number of input frames.
old-location: audio\iaudioprocessingobjectrt_calcoutputframes.htm
old-project: audio
ms.assetid: af558f8c-a38e-44d0-ad50-5e650f86cf2e
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: CalcOutputFrames, CalcOutputFrames method [Audio Devices], CalcOutputFrames method [Audio Devices],IAudioProcessingObjectRT interface, IAudioProcessingObjectRT interface [Audio Devices],CalcOutputFrames method, IAudioProcessingObjectRT.CalcOutputFrames, IAudioProcessingObjectRT::CalcOutputFrames, audio.iaudioprocessingobjectrt_calcoutputframes, audio_syseffects_r_1352a553-5788-46cb-be25-1d3d8e6ab963.xml, audioenginebaseapo/IAudioProcessingObjectRT::CalcOutputFrames
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: APO_FLAG
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
product: Windows
targetos: Windows
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: All levels
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



