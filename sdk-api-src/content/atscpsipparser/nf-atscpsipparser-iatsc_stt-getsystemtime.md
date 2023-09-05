---
UID: NF:atscpsipparser.IATSC_STT.GetSystemTime
title: IATSC_STT::GetSystemTime (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetSystemTime","GetSystemTime method [Microsoft TV Technologies]","GetSystemTime method [Microsoft TV Technologies]","IATSC_STT interface","IATSC_STT interface [Microsoft TV Technologies]","GetSystemTime method","IATSC_STT.GetSystemTime","IATSC_STT::GetSystemTime","IATSC_STTGetSystemTime","atscpsipparser/IATSC_STT::GetSystemTime","mstv.iatsc_stt_getsystemtime"]
old-location: mstv\iatsc_stt_getsystemtime.htm
tech.root: mstv
ms.assetid: 4add19d8-9626-468f-8b15-993fb51f3c13
ms.date: 12/05/2018
ms.keywords: GetSystemTime, GetSystemTime method [Microsoft TV Technologies], GetSystemTime method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetSystemTime method, IATSC_STT.GetSystemTime, IATSC_STT::GetSystemTime, IATSC_STTGetSystemTime, atscpsipparser/IATSC_STT::GetSystemTime, mstv.iatsc_stt_getsystemtime
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
 - IATSC_STT::GetSystemTime
 - atscpsipparser/IATSC_STT::GetSystemTime
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
 - IATSC_STT.GetSystemTime
---

# IATSC_STT::GetSystemTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSystemTime</b> method returns the current system time.

## -parameters

### -param pmdtSystemTime [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_date_and_time">MPEG_DATE_AND_TIME</a> structure allocated by the caller. The method fills the structure with the system time.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_stt">IATSC_STT Interface</a>