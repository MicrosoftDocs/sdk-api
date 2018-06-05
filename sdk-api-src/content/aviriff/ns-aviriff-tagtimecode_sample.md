---
UID: NS:aviriff.tagTIMECODE_SAMPLE
title: tagTIMECODE_SAMPLE
author: windows-sdk-content
description: The TIMECODE_SAMPLE structure contains complete timecode information.
old-location: dshow\timecode_sample.htm
old-project: DirectShow
ms.assetid: 7b17e152-99eb-4d6d-a8b1-bf4ef7ab83be
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: AM_TIMECODE_COLORFRAME, AM_TIMECODE_COLORSEQUENCE, AM_TIMECODE_FILMSEQUENCE_TYPE, AM_TIMECODE_FLAG_CF, AM_TIMECODE_FLAG_DF, AM_TIMECODE_FLAG_FCM, AM_TIMECODE_FLAG_FIELD, ED_DEVCAP_ATN_READ, ED_DEVCAP_RTC_READ, ED_DEVCAP_TIMECODE_READ, TIMECODE_SAMPLE, TIMECODE_SAMPLE structure [DirectShow], TIMECODE_SAMPLEStructure, aviriff/TIMECODE_SAMPLE, dshow.timecode_sample, tagTIMECODE_SAMPLE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: aviriff.h
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
tech.root: 
req.typenames: TIMECODE_SAMPLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	aviriff.h
api_name:
-	TIMECODE_SAMPLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTIMECODE_SAMPLE structure


## -description



The <code>TIMECODE_SAMPLE</code> structure contains complete timecode information.




## -struct-fields




### -field qwTick

Reference time, in 100-nanosecond units.


### -field timecode


<a href="https://msdn.microsoft.com/library/windows/hardware/ff568520">TIMECODE</a> structure.


### -field dwUser

Packed SMPTE userbits.


### -field dwFlags

Timecode flag masks. Specify one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_FCM"></a><a id="am_timecode_flag_fcm"></a><dl>
<dt><b>AM_TIMECODE_FLAG_FCM</b></dt>
</dl>
</td>
<td width="60%">
Frame code mode; 0 = nondrop; 1 = drop.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_CF"></a><a id="am_timecode_flag_cf"></a><dl>
<dt><b>AM_TIMECODE_FLAG_CF</b></dt>
</dl>
</td>
<td width="60%">
Color frame flag.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_FIELD"></a><a id="am_timecode_flag_field"></a><dl>
<dt><b>AM_TIMECODE_FLAG_FIELD</b></dt>
</dl>
</td>
<td width="60%">
Field flag.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_DF"></a><a id="am_timecode_flag_df"></a><dl>
<dt><b>AM_TIMECODE_FLAG_DF</b></dt>
</dl>
</td>
<td width="60%">
Drop frame flag (from flags in actual timecode on external media).

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_COLORFRAME"></a><a id="am_timecode_colorframe"></a><dl>
<dt><b>AM_TIMECODE_COLORFRAME</b></dt>
</dl>
</td>
<td width="60%">
Specifies frame in color sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_COLORSEQUENCE"></a><a id="am_timecode_colorsequence"></a><dl>
<dt><b>AM_TIMECODE_COLORSEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
Duration in frames of complete sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FILMSEQUENCE_TYPE"></a><a id="am_timecode_filmsequence_type"></a><dl>
<dt><b>AM_TIMECODE_FILMSEQUENCE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
One of the FILM_SEQUENCE_XXX defines.

</td>
</tr>
<tr>
<td width="40%"><a id="ED_DEVCAP_TIMECODE_READ"></a><a id="ed_devcap_timecode_read"></a><dl>
<dt><b>ED_DEVCAP_TIMECODE_READ</b></dt>
</dl>
</td>
<td width="60%">
Read SMPTE timecode; applies to DV camcorders.

</td>
</tr>
<tr>
<td width="40%"><a id="ED_DEVCAP_ATN_READ"></a><a id="ed_devcap_atn_read"></a><dl>
<dt><b>ED_DEVCAP_ATN_READ</b></dt>
</dl>
</td>
<td width="60%">
Read the absolute track number (ATN); applies to DV camcorders. This constant is defined in the header file Xprtdefs.h.

</td>
</tr>
<tr>
<td width="40%"><a id="ED_DEVCAP_RTC_READ"></a><a id="ed_devcap_rtc_read"></a><dl>
<dt><b>ED_DEVCAP_RTC_READ</b></dt>
</dl>
</td>
<td width="60%">
Read the relative time counter (RTC); applies to MPEG camcorders. This constant is defined in the header file Xprtdefs.h.

</td>
</tr>
</table>
 


## -remarks



The upper 16 bits in <b>dwFlags</b> are reserved; set to zero.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/c4ed646f-677e-4703-8197-036636f20561">IAMTimecodeReader::GetTimecode</a>
 

 

