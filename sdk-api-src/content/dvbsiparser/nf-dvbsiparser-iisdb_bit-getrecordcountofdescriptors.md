---
UID: NF:dvbsiparser.IISDB_BIT.GetRecordCountOfDescriptors
title: IISDB_BIT::GetRecordCountOfDescriptors (dvbsiparser.h)
description: Returns the number of descriptors for subtables in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IISDB_BIT.GetRecordCountOfDescriptors","IISDB_BIT::GetRecordCountOfDescriptors","dvbsiparser/IISDB_BIT::GetRecordCountOfDescriptors","mstv.iisdb_bit_getrecordcountofdescriptors"]
old-location: mstv\iisdb_bit_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 08df6f74-dbeb-4d32-8b0f-4ec88d35ff36
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IISDB_BIT.GetRecordCountOfDescriptors, IISDB_BIT::GetRecordCountOfDescriptors, dvbsiparser/IISDB_BIT::GetRecordCountOfDescriptors, mstv.iisdb_bit_getrecordcountofdescriptors
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
 - IISDB_BIT::GetRecordCountOfDescriptors
 - dvbsiparser/IISDB_BIT::GetRecordCountOfDescriptors
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
 - IISDB_BIT.GetRecordCountOfDescriptors
---

# IISDB_BIT::GetRecordCountOfDescriptors


## -description

Returns the number of descriptors for subtables in
  an Integrated Services Digital Broadcasting (ISDB)
  broadcaster information table (BIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a> 

  method to get the number of records in the BIT.

### -param pdwVal [out]

Receives the number of descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>