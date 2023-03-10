---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordKeys
title: IISDB_NBIT::GetRecordKeys (dvbsiparser.h)
description: Gets the number_of_keys field from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetRecordKeys","GetRecordKeys method [Microsoft TV Technologies]","GetRecordKeys method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordKeys method","IISDB_NBIT.GetRecordKeys","IISDB_NBIT::GetRecordKeys","dvbsiparser/IISDB_NBIT::GetRecordKeys","mstv.iisdb_nbit_getrecordkeys"]
old-location: mstv\iisdb_nbit_getrecordkeys.htm
tech.root: mstv
ms.assetid: c8f58c17-b3b1-4fc8-b6e0-2ab23681280d
ms.date: 12/05/2018
ms.keywords: GetRecordKeys, GetRecordKeys method [Microsoft TV Technologies], GetRecordKeys method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordKeys method, IISDB_NBIT.GetRecordKeys, IISDB_NBIT::GetRecordKeys, dvbsiparser/IISDB_NBIT::GetRecordKeys, mstv.iisdb_nbit_getrecordkeys
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
 - IISDB_NBIT::GetRecordKeys
 - dvbsiparser/IISDB_NBIT::GetRecordKeys
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
 - IISDB_NBIT.GetRecordKeys
---

# IISDB_NBIT::GetRecordKeys


## -description

Gets the number_of_keys field from a record in an Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
    Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a> method to get the number
    of records in the NBIT.

### -param pbKeys [out]

Gets the number_of_keys field from the NBIT record.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a>