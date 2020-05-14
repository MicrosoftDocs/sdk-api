---
UID: NF:bdaiface.IBDA_Encoder.GetState
title: IBDA_Encoder::GetState (bdaiface.h)
description: Queries the current state of the Encoder Service.helpviewer_keywords: ["GetState","GetState method [Microsoft TV Technologies]","GetState method [Microsoft TV Technologies]","IBDA_Encoder interface","IBDA_Encoder interface [Microsoft TV Technologies]","GetState method","IBDA_Encoder.GetState","IBDA_Encoder::GetState","PBDA_Encoder_BitrateMode_Average","PBDA_Encoder_BitrateMode_Constant","PBDA_Encoder_BitrateMode_Variable","bdaiface/IBDA_Encoder::GetState","mstv.ibda_encoder_getstate"]
old-location: mstv\ibda_encoder_getstate.htm
tech.root: mstv
ms.assetid: f3fdb3cc-2d7a-4fc3-b33c-feb1524479ec
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Microsoft TV Technologies], GetState method [Microsoft TV Technologies],IBDA_Encoder interface, IBDA_Encoder interface [Microsoft TV Technologies],GetState method, IBDA_Encoder.GetState, IBDA_Encoder::GetState, PBDA_Encoder_BitrateMode_Average, PBDA_Encoder_BitrateMode_Constant, PBDA_Encoder_BitrateMode_Variable, bdaiface/IBDA_Encoder::GetState, mstv.ibda_encoder_getstate
f1_keywords:
- bdaiface/IBDA_Encoder.GetState
dev_langs:
- c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdaiface.h
api_name:
- IBDA_Encoder.GetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_Encoder::GetState


## -description


Queries the current state of the Encoder Service.


## -parameters




### -param AudioBitrateMax [out]

Receives the maximum audio bit rate.


### -param AudioBitrateMin [out]

Receives the minimum audio bit rate.


### -param AudioBitrateMode [out]

Receives the audio compression mode. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_BitrateMode_Constant"></a><a id="pbda_encoder_bitratemode_constant"></a><a id="PBDA_ENCODER_BITRATEMODE_CONSTANT"></a><dl>
<dt><b>PBDA_Encoder_BitrateMode_Constant</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Constant bit rate (CBR) mode.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_BitrateMode_Variable"></a><a id="pbda_encoder_bitratemode_variable"></a><a id="PBDA_ENCODER_BITRATEMODE_VARIABLE"></a><dl>
<dt><b>PBDA_Encoder_BitrateMode_Variable</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Variable bit rate (VBR) mode.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_BitrateMode_Average"></a><a id="pbda_encoder_bitratemode_average"></a><a id="PBDA_ENCODER_BITRATEMODE_AVERAGE"></a><dl>
<dt><b>PBDA_Encoder_BitrateMode_Average</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Average bit rate (ABR) mode.

</td>
</tr>
</table>
 


### -param AudioBitrateStepping [out]

Receives the minimum increment for the audio bit rate.


### -param AudioBitrate [out]

Receives the audio bit rate.


### -param AudioMethodID [out]

Receives the active audio encoder method.


### -param AvailableAudioPrograms [out]

Receives the number of audio programs available to the encoder.


### -param AudioProgram [out]

Receives the program number of the audio program that is currently being encoded.


### -param VideoBitrateMax [out]

Receives the maximum video bit rate.


### -param VideoBitrateMin [out]

Receives the minimum video bit rate.


### -param VideoBitrateMode [out]

Receives the video compression mode. For a list of values, see <i>AudioBitrateMode</i>.


### -param VideoBitrate [out]

Receives the video bit rate.


### -param VideoBitrateStepping [out]

Receives the minimum increment for the video bit rate.


### -param VideoMethodID [out]

Receives the active video encoder method.


### -param SignalSourceID [out]

Receives the identifier of the signal source. The value is an auxiliary connector ID, as returned by the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_aux-enumcapability">IBDA_AUX::EnumCapability</a>  method.


### -param SignalFormat [out]

Receives a value from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a> enumeration. This value specifies the analog video standard that is received on the auxiliary input.


### -param SignalLock [out]

Receives the value <b>TRUE</b> if the device has a signal lock, and <b>FALSE</b> otherwise.


### -param SignalLevel [out]

Receives the signal level in decibels.


### -param SignalToNoiseRatio [out]

Receives a value between 0 and 100, indicating the signal-to-noise ratio.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_encoder">IBDA_Encoder</a>
 

 

