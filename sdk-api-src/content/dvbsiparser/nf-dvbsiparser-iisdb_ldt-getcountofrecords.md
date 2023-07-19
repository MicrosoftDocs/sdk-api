---
UID: NF:dvbsiparser.IISDB_LDT.GetCountOfRecords
title: IISDB_LDT::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT). An LDT contains data used to collect reference information from other tables.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetCountOfRecords method","IISDB_LDT.GetCountOfRecords","IISDB_LDT::GetCountOfRecords","dvbsiparser/IISDB_LDT::GetCountOfRecords","mstv.iisdb_ldt_getcountofrecords"]
old-location: mstv\iisdb_ldt_getcountofrecords.htm
tech.root: mstv
ms.assetid: da91deea-527c-4458-9db5-ae500cee19bb
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetCountOfRecords method, IISDB_LDT.GetCountOfRecords, IISDB_LDT::GetCountOfRecords, dvbsiparser/IISDB_LDT::GetCountOfRecords, mstv.iisdb_ldt_getcountofrecords
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
 - IISDB_LDT::GetCountOfRecords
 - dvbsiparser/IISDB_LDT::GetCountOfRecords
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
 - IISDB_LDT.GetCountOfRecords
---

# IISDB_LDT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in an
  Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). An LDT contains data used to collect reference
  information from other tables.

## -parameters

### -param pdwVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>