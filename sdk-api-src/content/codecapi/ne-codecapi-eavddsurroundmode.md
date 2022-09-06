---
UID: NE:codecapi.eAVDDSurroundMode
title: eAVDDSurroundMode (codecapi.h)
description: Specifies whether the audio is encoded in Dolby Surround. This enumeration is used with the AVDDSurroundMode property.
helpviewer_keywords: ["codecapi/eAVDDSurroundMode","codecapi/eAVDDSurroundMode_No","codecapi/eAVDDSurroundMode_NotIndicated","codecapi/eAVDDSurroundMode_Yes","dshow.eavddsurroundmode","eAVDDSurroundMode","eAVDDSurroundMode enumeration [DirectShow]","eAVDDSurroundModeEnumeration","eAVDDSurroundMode_No","eAVDDSurroundMode_NotIndicated","eAVDDSurroundMode_Yes"]
old-location: dshow\eavddsurroundmode.htm
tech.root: dshow
ms.assetid: daebcbdf-3a4d-494a-a403-8b075a6d393b
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDDSurroundMode, codecapi/eAVDDSurroundMode_No, codecapi/eAVDDSurroundMode_NotIndicated, codecapi/eAVDDSurroundMode_Yes, dshow.eavddsurroundmode, eAVDDSurroundMode, eAVDDSurroundMode enumeration [DirectShow], eAVDDSurroundModeEnumeration, eAVDDSurroundMode_No, eAVDDSurroundMode_NotIndicated, eAVDDSurroundMode_Yes
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - eAVDDSurroundMode
 - codecapi/eAVDDSurroundMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDDSurroundMode
---

# eAVDDSurroundMode enumeration


## -description

Specifies whether the audio is encoded in Dolby Surround. This enumeration is used with the <a href="/windows/desktop/DirectShow/avddsurroundmode-property">AVDDSurroundMode</a> property.

## -enum-fields

### -field eAVDDSurroundMode_NotIndicated:0

The bit stream does not indicate whether the audio is encoded in Dolby Surround.

### -field eAVDDSurroundMode_No:1

The bit stream is not encoded in Dolby Surround.

### -field eAVDDSurroundMode_Yes:2

The bit stream is encoded in Dolby Surround.

## -remarks

If the audio stream is Dolby AC-3, this property reflects the value of the dsurmod field in the bit stream.

<table>
<tr>
<th>Bit field
            </th>
<th>Value
            </th>
</tr>
<tr>
<td>00</td>
<td>eAVDDSurroundMode_NotIndicated</td>
</tr>
<tr>
<td>01</td>
<td>eAVDDSurroundMode_No</td>
</tr>
<tr>
<td>10</td>
<td>eAVDDSurroundMode_Yes</td>
</tr>
</table>
 

If the audio stream is any other format, the value is eAVDDSurroundMode_No.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
