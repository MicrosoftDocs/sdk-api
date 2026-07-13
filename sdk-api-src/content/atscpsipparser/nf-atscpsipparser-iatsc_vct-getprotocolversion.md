---
UID: NF:atscpsipparser.IATSC_VCT.GetProtocolVersion
title: IATSC_VCT::GetProtocolVersion (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetProtocolVersion","GetProtocolVersion method [Microsoft TV Technologies]","GetProtocolVersion method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetProtocolVersion method","IATSC_VCT.GetProtocolVersion","IATSC_VCT::GetProtocolVersion","IATSC_VCTGetProtocolVersion","atscpsipparser/IATSC_VCT::GetProtocolVersion","mstv.iatsc_vct_getprotocolversion"]
old-location: mstv\iatsc_vct_getprotocolversion.htm
tech.root: mstv
ms.assetid: 51bfc546-9150-4063-b8a4-2dc1238070d0
ms.date: 12/05/2018
ms.keywords: GetProtocolVersion, GetProtocolVersion method [Microsoft TV Technologies], GetProtocolVersion method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetProtocolVersion method, IATSC_VCT.GetProtocolVersion, IATSC_VCT::GetProtocolVersion, IATSC_VCTGetProtocolVersion, atscpsipparser/IATSC_VCT::GetProtocolVersion, mstv.iatsc_vct_getprotocolversion
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
 - IATSC_VCT::GetProtocolVersion
 - atscpsipparser/IATSC_VCT::GetProtocolVersion
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
 - IATSC_VCT.GetProtocolVersion
---

# IATSC_VCT::GetProtocolVersion


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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>