---
UID: NF:dvbsiparser.IISDB_NBIT.GetCountOfRecords
title: IISDB_NBIT::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetCountOfRecords method","IISDB_NBIT.GetCountOfRecords","IISDB_NBIT::GetCountOfRecords","dvbsiparser/IISDB_NBIT::GetCountOfRecords","mstv.iisdb_nbit_getcountofrecords"]
old-location: mstv\iisdb_nbit_getcountofrecords.htm
tech.root: mstv
ms.assetid: c747278a-dea7-4772-b37d-89c1deaaf91f
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetCountOfRecords method, IISDB_NBIT.GetCountOfRecords, IISDB_NBIT::GetCountOfRecords, dvbsiparser/IISDB_NBIT::GetCountOfRecords, mstv.iisdb_nbit_getcountofrecords
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
 - IISDB_NBIT::GetCountOfRecords
 - dvbsiparser/IISDB_NBIT::GetCountOfRecords
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
 - IISDB_NBIT.GetCountOfRecords
---

# IISDB_NBIT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).

## -parameters

### -param pdwVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>