---
UID: NF:dvbsiparser.IISDB_BIT.GetRecordBroadcasterId
title: IISDB_BIT::GetRecordBroadcasterId (dvbsiparser.h)
description: Gets the broadcaster_id field from a record in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetRecordBroadcasterId","GetRecordBroadcasterId method [Microsoft TV Technologies]","GetRecordBroadcasterId method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetRecordBroadcasterId method","IISDB_BIT.GetRecordBroadcasterId","IISDB_BIT::GetRecordBroadcasterId","dvbsiparser/IISDB_BIT::GetRecordBroadcasterId","mstv.iisdb_bit_getrecordbroadcasterid"]
old-location: mstv\iisdb_bit_getrecordbroadcasterid.htm
tech.root: mstv
ms.assetid: 9decce55-599b-42c2-a715-84a6f4eefc33
ms.date: 12/05/2018
ms.keywords: GetRecordBroadcasterId, GetRecordBroadcasterId method [Microsoft TV Technologies], GetRecordBroadcasterId method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetRecordBroadcasterId method, IISDB_BIT.GetRecordBroadcasterId, IISDB_BIT::GetRecordBroadcasterId, dvbsiparser/IISDB_BIT::GetRecordBroadcasterId, mstv.iisdb_bit_getrecordbroadcasterid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IISDB_BIT::GetRecordBroadcasterId
 - dvbsiparser/IISDB_BIT::GetRecordBroadcasterId
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
 - IISDB_BIT.GetRecordBroadcasterId
---

# IISDB_BIT::GetRecordBroadcasterId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the broadcaster_id field from
  a record in an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a> method to get the number of records in the BIT.

### -param pbVal [out]

Receives the broadcaster_id field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>