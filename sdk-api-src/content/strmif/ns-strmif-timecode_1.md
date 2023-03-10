---
UID: NS:strmif._timecode
title: TIMECODE (strmif.h)
description: The TIMECODE structure contains basic timecode frame count information.T
helpviewer_keywords: ["*PTIMECODE","ED_FORMAT_SMPTE_24","ED_FORMAT_SMPTE_25","ED_FORMAT_SMPTE_30","ED_FORMAT_SMPTE_30DROP","TIMECODE","TIMECODE structure [DirectShow]","TIMECODEStructure","dshow.timecode","strmif/TIMECODE","tagTIMECODE"]
old-location: dshow\timecode.htm
tech.root: dshow
ms.assetid: 652be387-aa5e-4077-8b2d-b08bc40b31bb
ms.date: 12/05/2018
ms.keywords: '*PTIMECODE, ED_FORMAT_SMPTE_24, ED_FORMAT_SMPTE_25, ED_FORMAT_SMPTE_30, ED_FORMAT_SMPTE_30DROP, TIMECODE, TIMECODE structure [DirectShow], TIMECODEStructure, dshow.timecode, strmif/TIMECODE, tagTIMECODE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TIMECODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _timecode
 - strmif/_timecode
 - TIMECODE
 - strmif/TIMECODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - TIMECODE
---

# TIMECODE structure


## -description

The <b>TIMECODE</b> structure contains basic timecode frame count information.

## -struct-fields

### -field wFrameRate

Number of frames per second. Specify with one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_30"></a><a id="ed_format_smpte_30"></a><dl>
<dt><b>ED_FORMAT_SMPTE_30</b></dt>
</dl>
</td>
<td width="60%">
30 frames per second. 

</td>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_30DROP"></a><a id="ed_format_smpte_30drop"></a><dl>
<dt><b>ED_FORMAT_SMPTE_30DROP</b></dt>
</dl>
</td>
<td width="60%">
30 frames per second drop frame (actual rate 29.97 fps). 

</td>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_25"></a><a id="ed_format_smpte_25"></a><dl>
<dt><b>ED_FORMAT_SMPTE_25</b></dt>
</dl>
</td>
<td width="60%">
25 frames per second. 

</td>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_24"></a><a id="ed_format_smpte_24"></a><dl>
<dt><b>ED_FORMAT_SMPTE_24</b></dt>
</dl>
</td>
<td width="60%">
24 frames per second. 

</td>
</tr>
</table>

### -field wFrameFract

Fractional frame. Full scale is 0x1000.

### -field dwFrames

Timecode value as a binary framecount.

### -field qw

## -remarks

Fractional frame can be used to indicate temporal offset into frame when timecode was actually read from an external device; for example, wFrameFract=0x7ff means the timecode value was read from the device at the end of the first video field.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
