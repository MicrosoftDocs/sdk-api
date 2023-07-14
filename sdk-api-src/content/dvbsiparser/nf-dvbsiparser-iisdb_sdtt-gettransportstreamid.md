---
UID: NF:dvbsiparser.IISDB_SDTT.GetTransportStreamId
title: IISDB_SDTT::GetTransportStreamId (dvbsiparser.h)
description: Returns the transport stream identifier (TSID) for an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetTransportStreamId","GetTransportStreamId method [Microsoft TV Technologies]","GetTransportStreamId method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetTransportStreamId method","IISDB_SDTT.GetTransportStreamId","IISDB_SDTT::GetTransportStreamId","dvbsiparser/IISDB_SDTT::GetTransportStreamId","mstv.iisdb_sdtt_gettransportstreamid"]
old-location: mstv\iisdb_sdtt_gettransportstreamid.htm
tech.root: mstv
ms.assetid: d73b705f-8409-438e-9f30-3bf2bbf86404
ms.date: 12/05/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetTransportStreamId method, IISDB_SDTT.GetTransportStreamId, IISDB_SDTT::GetTransportStreamId, dvbsiparser/IISDB_SDTT::GetTransportStreamId, mstv.iisdb_sdtt_gettransportstreamid
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IISDB_SDTT::GetTransportStreamId
 - dvbsiparser/IISDB_SDTT::GetTransportStreamId
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
 - IISDB_SDTT.GetTransportStreamId
---

# IISDB_SDTT::GetTransportStreamId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns the transport stream identifier (TSID) for
  an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).

## -parameters

### -param pwVal [out]

Receives the transport_stream_id field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>