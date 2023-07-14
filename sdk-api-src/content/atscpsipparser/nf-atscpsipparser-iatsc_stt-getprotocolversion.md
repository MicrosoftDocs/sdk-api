---
UID: NF:atscpsipparser.IATSC_STT.GetProtocolVersion
title: IATSC_STT::GetProtocolVersion (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetProtocolVersion","GetProtocolVersion method [Microsoft TV Technologies]","GetProtocolVersion method [Microsoft TV Technologies]","IATSC_STT interface","IATSC_STT interface [Microsoft TV Technologies]","GetProtocolVersion method","IATSC_STT.GetProtocolVersion","IATSC_STT::GetProtocolVersion","IATSC_STTGetProtocolVersion","atscpsipparser/IATSC_STT::GetProtocolVersion","mstv.iatsc_stt_getprotocolversion"]
old-location: mstv\iatsc_stt_getprotocolversion.htm
tech.root: mstv
ms.assetid: c735400d-9227-4f13-9703-ddafdf5772b0
ms.date: 12/05/2018
ms.keywords: GetProtocolVersion, GetProtocolVersion method [Microsoft TV Technologies], GetProtocolVersion method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetProtocolVersion method, IATSC_STT.GetProtocolVersion, IATSC_STT::GetProtocolVersion, IATSC_STTGetProtocolVersion, atscpsipparser/IATSC_STT::GetProtocolVersion, mstv.iatsc_stt_getprotocolversion
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
 - IATSC_STT::GetProtocolVersion
 - atscpsipparser/IATSC_STT::GetProtocolVersion
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
 - IATSC_STT.GetProtocolVersion
---

# IATSC_STT::GetProtocolVersion


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetProtocolVersion</b> method returns the protocol version of the table.

## -parameters

### -param pbVal [out]

Receives the protocol_version field.

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