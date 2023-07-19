---
UID: NF:atscpsipparser.IATSC_STT.GetGpsUtcOffset
title: IATSC_STT::GetGpsUtcOffset (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetGpsUtcOffset","GetGpsUtcOffset method [Microsoft TV Technologies]","GetGpsUtcOffset method [Microsoft TV Technologies]","IATSC_STT interface","IATSC_STT interface [Microsoft TV Technologies]","GetGpsUtcOffset method","IATSC_STT.GetGpsUtcOffset","IATSC_STT::GetGpsUtcOffset","IATSC_STTGetGpsUtcOffset","atscpsipparser/IATSC_STT::GetGpsUtcOffset","mstv.iatsc_stt_getgpsutcoffset"]
old-location: mstv\iatsc_stt_getgpsutcoffset.htm
tech.root: mstv
ms.assetid: 124c864a-a504-4f3c-836f-bdbe730beda7
ms.date: 12/05/2018
ms.keywords: GetGpsUtcOffset, GetGpsUtcOffset method [Microsoft TV Technologies], GetGpsUtcOffset method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetGpsUtcOffset method, IATSC_STT.GetGpsUtcOffset, IATSC_STT::GetGpsUtcOffset, IATSC_STTGetGpsUtcOffset, atscpsipparser/IATSC_STT::GetGpsUtcOffset, mstv.iatsc_stt_getgpsutcoffset
req.header: atscpsipparser.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IATSC_STT::GetGpsUtcOffset
 - atscpsipparser/IATSC_STT::GetGpsUtcOffset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_STT.GetGpsUtcOffset
---

# IATSC_STT::GetGpsUtcOffset


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetGpsUtcOffset</b> method returns the current offset between Global Positioning Satellite (GPS) time and Universal Time Coordinated (UTC), in seconds.

## -parameters

### -param pbVal [out]

Receives the GPS_UTC_offset field.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

GPS time is measured in seconds since January 6, 1980, and is not adjusted for leap seconds. To convert GPS time to UTC, which is adjusted for leap seconds, subtract the offset from GPS time.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_stt">IATSC_STT Interface</a>