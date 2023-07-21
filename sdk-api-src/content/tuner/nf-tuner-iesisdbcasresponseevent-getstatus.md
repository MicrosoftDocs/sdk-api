---
UID: NF:tuner.IESIsdbCasResponseEvent.GetStatus
title: IESIsdbCasResponseEvent::GetStatus (tuner.h)
description: Gets the response status returned in an IsdbCasResponse event.
helpviewer_keywords: ["GetStatus","GetStatus method [DirectShow]","GetStatus method [DirectShow]","IESIsdbCasResponseEvent interface","IESIsdbCasResponseEvent interface [DirectShow]","GetStatus method","IESIsdbCasResponseEvent.GetStatus","IESIsdbCasResponseEvent::GetStatus","mstv.iesisdbcasresponseevent_getstatus","tuner/IESIsdbCasResponseEvent::GetStatus"]
old-location: mstv\iesisdbcasresponseevent_getstatus.htm
tech.root: mstv
ms.assetid: 63cf3d47-5aac-4bce-8562-f67df47f83b2
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [DirectShow], GetStatus method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetStatus method, IESIsdbCasResponseEvent.GetStatus, IESIsdbCasResponseEvent::GetStatus, mstv.iesisdbcasresponseevent_getstatus, tuner/IESIsdbCasResponseEvent::GetStatus
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IESIsdbCasResponseEvent::GetStatus
 - tuner/IESIsdbCasResponseEvent::GetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESIsdbCasResponseEvent.GetStatus
---

# IESIsdbCasResponseEvent::GetStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the response status returned in an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IsdbCasResponse</a> event.

## -parameters

### -param pStatus [out, retval]

Receives the status code. This can have any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x9000</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6400</dt>
</dl>
</td>
<td width="60%">
Memory error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6581</dt>
</dl>
</td>
<td width="60%">
Write error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6700</dt>
</dl>
</td>
<td width="60%">
Interconnect command length.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6800</dt>
</dl>
</td>
<td width="60%">
Unsupported class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6A86</dt>
</dl>
</td>
<td width="60%">
Incorrect parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6D00</dt>
</dl>
</td>
<td width="60%">
Unsupported instruction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6E00</dt>
</dl>
</td>
<td width="60%">
Unsupported class.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IESIsdbCasResponseEvent</a>