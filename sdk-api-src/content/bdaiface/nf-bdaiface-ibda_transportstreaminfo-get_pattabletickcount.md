---
UID: NF:bdaiface.IBDA_TransportStreamInfo.get_PatTableTickCount
title: IBDA_TransportStreamInfo::get_PatTableTickCount (bdaiface.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IBDA_TransportStreamInfo interface [Microsoft TV Technologies]","get_PatTableTickCount method","IBDA_TransportStreamInfo.get_PatTableTickCount","IBDA_TransportStreamInfo::get_PatTableTickCount","IBDA_TransportStreamInfoget_PatTableTickCount","bdaiface/IBDA_TransportStreamInfo::get_PatTableTickCount","get_PatTableTickCount","get_PatTableTickCount method [Microsoft TV Technologies]","get_PatTableTickCount method [Microsoft TV Technologies]","IBDA_TransportStreamInfo interface","mstv.ibda_transportstreaminfo_get_pattabletickcount"]
old-location: mstv\ibda_transportstreaminfo_get_pattabletickcount.htm
tech.root: mstv
ms.assetid: 8ad1a680-0037-40d5-9263-2a2f0862154c
ms.date: 12/05/2018
ms.keywords: IBDA_TransportStreamInfo interface [Microsoft TV Technologies],get_PatTableTickCount method, IBDA_TransportStreamInfo.get_PatTableTickCount, IBDA_TransportStreamInfo::get_PatTableTickCount, IBDA_TransportStreamInfoget_PatTableTickCount, bdaiface/IBDA_TransportStreamInfo::get_PatTableTickCount, get_PatTableTickCount, get_PatTableTickCount method [Microsoft TV Technologies], get_PatTableTickCount method [Microsoft TV Technologies],IBDA_TransportStreamInfo interface, mstv.ibda_transportstreaminfo_get_pattabletickcount
req.header: bdaiface.h
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
 - IBDA_TransportStreamInfo::get_PatTableTickCount
 - bdaiface/IBDA_TransportStreamInfo::get_PatTableTickCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_TransportStreamInfo.get_PatTableTickCount
---

# IBDA_TransportStreamInfo::get_PatTableTickCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_PatTableTickCount</b> method returns the time when the most recent Program Association Table (PAT) section was received. The time is expressed in terms of the tick count, which is the number of milliseconds that have elapsed since the system was started. For more information, see <b>GetTickCount</b> in the Platform SDK documentation.

## -parameters

### -param pPatTickCount [out]

Receives the tick count when the last PAT section was received.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_transportstreaminfo">IBDA_TransportStreamInfo Interface</a>