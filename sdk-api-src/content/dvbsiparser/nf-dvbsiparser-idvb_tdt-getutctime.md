---
UID: NF:dvbsiparser.IDVB_TDT.GetUTCTime
title: IDVB_TDT::GetUTCTime (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetUTCTime","GetUTCTime method [Microsoft TV Technologies]","GetUTCTime method [Microsoft TV Technologies]","IDVB_TDT interface","IDVB_TDT interface [Microsoft TV Technologies]","GetUTCTime method","IDVB_TDT.GetUTCTime","IDVB_TDT::GetUTCTime","IDVB_TDTGetUTCTime","dvbsiparser/IDVB_TDT::GetUTCTime","mstv.idvb_tdt_getutctime"]
old-location: mstv\idvb_tdt_getutctime.htm
tech.root: mstv
ms.assetid: a3c45e91-3e30-4f22-aedb-d81024160e88
ms.date: 12/05/2018
ms.keywords: GetUTCTime, GetUTCTime method [Microsoft TV Technologies], GetUTCTime method [Microsoft TV Technologies],IDVB_TDT interface, IDVB_TDT interface [Microsoft TV Technologies],GetUTCTime method, IDVB_TDT.GetUTCTime, IDVB_TDT::GetUTCTime, IDVB_TDTGetUTCTime, dvbsiparser/IDVB_TDT::GetUTCTime, mstv.idvb_tdt_getutctime
req.header: dvbsiparser.h
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
 - IDVB_TDT::GetUTCTime
 - dvbsiparser/IDVB_TDT::GetUTCTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_TDT.GetUTCTime
---

# IDVB_TDT::GetUTCTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetUTCTime</b> method returns the current UTC time and date.

## -parameters

### -param pmdtVal [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_date_and_time">MPEG_DATE_AND_TIME</a> structure allocated by the caller. The method fills the structure with the UTC time and date.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_tdt">IDVB_TDT Interface</a>