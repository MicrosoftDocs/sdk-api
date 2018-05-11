---
UID: NE:strmif._AM_AUDIO_RENDERER_STAT_PARAM
title: "_AM_AUDIO_RENDERER_STAT_PARAM"
author: windows-driver-content
description: The _AM_AUDIO_RENDERER_STAT_PARAM enumeration specifies which performance information to retrieve from the audio renderer.
old-location: dshow\_am_audio_renderer_stat_param.htm
old-project: DirectShow
ms.assetid: ae090ab0-22e2-4407-8c16-feaa4fa20774
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AM_AUDREND_STAT_PARAM_BREAK_COUNT, AM_AUDREND_STAT_PARAM_BUFFERFULLNESS, AM_AUDREND_STAT_PARAM_DISCONTINUITIES, AM_AUDREND_STAT_PARAM_JITTER, AM_AUDREND_STAT_PARAM_LAST_BUFFER_DUR, AM_AUDREND_STAT_PARAM_SILENCE_DUR, AM_AUDREND_STAT_PARAM_SLAVE_ACCUMERROR, AM_AUDREND_STAT_PARAM_SLAVE_DROPWRITE_DUR, AM_AUDREND_STAT_PARAM_SLAVE_HIGHLOWERROR, AM_AUDREND_STAT_PARAM_SLAVE_LASTHIGHLOWERROR, AM_AUDREND_STAT_PARAM_SLAVE_MODE, AM_AUDREND_STAT_PARAM_SLAVE_RATE, _AM_AUDIO_RENDERER_STAT_PARAM, _AM_AUDIO_RENDERER_STAT_PARAM enumeration [DirectShow], _AM_AUDIO_RENDERER_STAT_PARAMEnumeration, dshow._am_audio_renderer_stat_param, strmif/AM_AUDREND_STAT_PARAM_BREAK_COUNT, strmif/AM_AUDREND_STAT_PARAM_BUFFERFULLNESS, strmif/AM_AUDREND_STAT_PARAM_DISCONTINUITIES, strmif/AM_AUDREND_STAT_PARAM_JITTER, strmif/AM_AUDREND_STAT_PARAM_LAST_BUFFER_DUR, strmif/AM_AUDREND_STAT_PARAM_SILENCE_DUR, strmif/AM_AUDREND_STAT_PARAM_SLAVE_ACCUMERROR, strmif/AM_AUDREND_STAT_PARAM_SLAVE_DROPWRITE_DUR, strmif/AM_AUDREND_STAT_PARAM_SLAVE_HIGHLOWERROR, strmif/AM_AUDREND_STAT_PARAM_SLAVE_LASTHIGHLOWERROR, strmif/AM_AUDREND_STAT_PARAM_SLAVE_MODE, strmif/AM_AUDREND_STAT_PARAM_SLAVE_RATE, strmif/_AM_AUDIO_RENDERER_STAT_PARAM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	_AM_AUDIO_RENDERER_STAT_PARAM
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# _AM_AUDIO_RENDERER_STAT_PARAM enumeration


## -description



The <b>_AM_AUDIO_RENDERER_STAT_PARAM</b> enumeration specifies which performance information to retrieve from the audio renderer.



This enumeration type is used in the <a href="https://msdn.microsoft.com/bc01cac7-316f-4d18-ae68-c3db4dbf03fa">IAMAudioRendererStats::GetStatParam</a> method. Each enumeration member defines the meaning of the values that are returned in the <i>pdwParam1</i> and <i>pdwParam2</i> parameters of <b>GetStatParam</b>.


## -enum-fields




### -field AM_AUDREND_STAT_PARAM_BREAK_COUNT

<i>Param1</i>: The cumulative number of breaks in the audio stream.

<i>Param2</i>: Not used.


### -field AM_AUDREND_STAT_PARAM_SLAVE_MODE

<i>Param1</i>: Indicates the current rate-matching mode. The value is a bitwise combination of the following:

<ul>
<li>0x00: No rate matching.</li>
<li>0x01: Match rates to a live source.</li>
<li>0x02: Match rates based on the rate of the incoming audio data.</li>
<li>0x04: Match rates with the filter graph's reference clock (when the clock is not provided by the audio renderer).</li>
<li>0x10: Match rates based on the time stamps of the audio samples.</li>
</ul>
<i>Param2</i>: Not used.


### -field AM_AUDREND_STAT_PARAM_SILENCE_DUR

<i>Param1</i>: The cumulative amount of silence the audio renderer has inserted, due to gaps in the time stamps of the incoming samples. The value is given in milliseconds.

<i>Param2</i>: Not used.


### -field AM_AUDREND_STAT_PARAM_LAST_BUFFER_DUR

<i>Param1</i>: The duration of the most recent audio buffer, in milliseconds.

<i>Param2</i>: Not used.


### -field AM_AUDREND_STAT_PARAM_DISCONTINUITIES

<i>Param1</i>: The cumulative number of discontinuities in the audio stream.

<i>Param2</i>: Not used.


### -field AM_AUDREND_STAT_PARAM_SLAVE_RATE

<i>Param1</i>: The sample rate that the audio renderer is matching, in samples per second.

<i>Param2</i>: Not used.

Valid only when the <a href="https://msdn.microsoft.com/ec6cc790-8c1f-4de4-a7ca-a7073894380e">DirectSound Renderer</a> is matching rates to another clock or a live source.


### -field AM_AUDREND_STAT_PARAM_SLAVE_DROPWRITE_DUR

<i>Param1</i>: The amount of data dropped to stay in sync, in milliseconds.

<i>Param2</i>: Not used.

Applies only when the <a href="https://msdn.microsoft.com/a3f2776b-974b-4886-82a3-38e00b607a07">Audio Renderer (WaveOut)</a> filter is matching rates to a master clock.


### -field AM_AUDREND_STAT_PARAM_SLAVE_HIGHLOWERROR

<i>Param1</i>: The highest difference noted between the audio renderer's clock and the clock it is trying to match.

<i>Param2</i>: The lowest difference noted between the audio renderer's clock and the clock it is trying to match.

Valid only when the audio renderer is matching rates to a master clock.


### -field AM_AUDREND_STAT_PARAM_SLAVE_LASTHIGHLOWERROR

<i>Param1</i>: The last high error, in milliseconds. A <i>high error</i> occurs when the audio renderer falls behind the clock.

<i>Param2</i>: The last low error, in milliseconds. A <i>low error</i> occurs when the audio renderer runs ahead of the clock. 

Valid only when the audio renderer is matching rates to a master clock.


### -field AM_AUDREND_STAT_PARAM_SLAVE_ACCUMERROR

<i>Param1</i>: The accumulated difference between the audio renderer and the master clock, including adjustments made by dropping samples or inserting gaps.

<i>Param2</i>: Not used.

Valid only when the audio renderer is matching rates to another clock or a live source.


### -field AM_AUDREND_STAT_PARAM_BUFFERFULLNESS

<i>Param1</i>: How much audio data is in the audio buffer, as a percentage.

<i>Param2</i>: Not used.


### -field AM_AUDREND_STAT_PARAM_JITTER

Not implemented.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/f5cca658-73ce-4f4d-8992-afb7824f4117">IAMAudioRendererStats Interface</a>
 

 

