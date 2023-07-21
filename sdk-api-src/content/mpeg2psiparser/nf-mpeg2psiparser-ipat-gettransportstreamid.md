---
UID: NF:mpeg2psiparser.IPAT.GetTransportStreamId
title: IPAT::GetTransportStreamId (mpeg2psiparser.h)
description: The GetTransportStreamId method returns the transport stream identifier (TSID) for the PAT.
helpviewer_keywords: ["GetTransportStreamId","GetTransportStreamId method [Microsoft TV Technologies]","GetTransportStreamId method [Microsoft TV Technologies]","IPAT interface","IPAT interface [Microsoft TV Technologies]","GetTransportStreamId method","IPAT.GetTransportStreamId","IPAT::GetTransportStreamId","IPATGetTransportStreamId","mpeg2psiparser/IPAT::GetTransportStreamId","mstv.ipat_gettransportstreamid"]
old-location: mstv\ipat_gettransportstreamid.htm
tech.root: mstv
ms.assetid: 3a13bb01-47d6-4737-9e66-169def727b5e
ms.date: 12/05/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetTransportStreamId method, IPAT.GetTransportStreamId, IPAT::GetTransportStreamId, IPATGetTransportStreamId, mpeg2psiparser/IPAT::GetTransportStreamId, mstv.ipat_gettransportstreamid
req.header: mpeg2psiparser.h
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
 - IPAT::GetTransportStreamId
 - mpeg2psiparser/IPAT::GetTransportStreamId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPAT.GetTransportStreamId
---

# IPAT::GetTransportStreamId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetTransportStreamId</b> method returns the transport stream identifier (TSID) for the PAT.

## -parameters

### -param pwVal [out]

Receives the transport_stream_id field.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipat">IPAT Interface</a>