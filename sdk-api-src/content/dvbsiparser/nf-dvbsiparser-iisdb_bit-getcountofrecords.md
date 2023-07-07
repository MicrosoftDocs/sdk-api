---
UID: NF:dvbsiparser.IISDB_BIT.GetCountOfRecords
title: IISDB_BIT::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetCountOfRecords method","IISDB_BIT.GetCountOfRecords","IISDB_BIT::GetCountOfRecords","dvbsiparser/IISDB_BIT::GetCountOfRecords","mstv.iisdb_bit_getcountofrecords"]
old-location: mstv\iisdb_bit_getcountofrecords.htm
tech.root: mstv
ms.assetid: 3f36c03a-462e-479a-ad8c-5322377dbca0
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetCountOfRecords method, IISDB_BIT.GetCountOfRecords, IISDB_BIT::GetCountOfRecords, dvbsiparser/IISDB_BIT::GetCountOfRecords, mstv.iisdb_bit_getcountofrecords
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
 - IISDB_BIT::GetCountOfRecords
 - dvbsiparser/IISDB_BIT::GetCountOfRecords
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
 - IISDB_BIT.GetCountOfRecords
---

# IISDB_BIT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in an
  Integrated Services Digital Broadcasting (ISDB)
  broadcaster information table
  (BIT).

## -parameters

### -param pdwVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>