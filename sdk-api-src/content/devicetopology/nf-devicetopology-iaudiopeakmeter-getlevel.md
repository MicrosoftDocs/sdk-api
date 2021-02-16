---
UID: NF:devicetopology.IAudioPeakMeter.GetLevel
title: IAudioPeakMeter::GetLevel (devicetopology.h)
description: The GetLevel method gets the peak level that the peak meter recorded for the specified channel since the peak level for that channel was previously read.
helpviewer_keywords: ["GetLevel","GetLevel method [Core Audio]","GetLevel method [Core Audio]","IAudioPeakMeter interface","IAudioPeakMeter interface [Core Audio]","GetLevel method","IAudioPeakMeter.GetLevel","IAudioPeakMeter::GetLevel","IAudioPeakMeterGetLevel","coreaudio.iaudiopeakmeter_getlevel","devicetopology/IAudioPeakMeter::GetLevel"]
old-location: coreaudio\iaudiopeakmeter_getlevel.htm
tech.root: CoreAudio
ms.assetid: c5d7d941-b001-49a9-b421-a999f90ddb22
ms.date: 12/05/2018
ms.keywords: GetLevel, GetLevel method [Core Audio], GetLevel method [Core Audio],IAudioPeakMeter interface, IAudioPeakMeter interface [Core Audio],GetLevel method, IAudioPeakMeter.GetLevel, IAudioPeakMeter::GetLevel, IAudioPeakMeterGetLevel, coreaudio.iaudiopeakmeter_getlevel, devicetopology/IAudioPeakMeter::GetLevel
req.header: devicetopology.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioPeakMeter::GetLevel
 - devicetopology/IAudioPeakMeter::GetLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioPeakMeter.GetLevel
---

# IAudioPeakMeter::GetLevel


## -description

The <b>GetLevel</b> method gets the peak level that the peak meter recorded for the specified channel since the peak level for that channel was previously read.

## -parameters

### -param nChannel [in]

The channel number. If the audio stream has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels in the stream, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiopeakmeter-getchannelcount">IAudioPeakMeter::GetChannelCount</a> method.

### -param pfLevel [out]

Pointer to a <b>float</b> variable into which the method writes the peak meter level in decibels.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nChannel</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pfLevel</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiopeakmeter">IAudioPeakMeter Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiopeakmeter-getchannelcount">IAudioPeakMeter::GetChannelCount</a>