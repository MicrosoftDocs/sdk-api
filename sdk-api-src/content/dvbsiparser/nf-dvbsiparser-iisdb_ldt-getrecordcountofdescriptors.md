---
UID: NF:dvbsiparser.IISDB_LDT.GetRecordCountOfDescriptors
title: IISDB_LDT::GetRecordCountOfDescriptors (dvbsiparser.h)
description: Returns the number of descriptors for a record in an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IISDB_LDT.GetRecordCountOfDescriptors","IISDB_LDT::GetRecordCountOfDescriptors","dvbsiparser/IISDB_LDT::GetRecordCountOfDescriptors","mstv.iisdb_ldt_getrecordcountofdescriptors"]
old-location: mstv\iisdb_ldt_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 1352eec0-fed2-4d14-81f2-c73b8d34a264
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IISDB_LDT.GetRecordCountOfDescriptors, IISDB_LDT::GetRecordCountOfDescriptors, dvbsiparser/IISDB_LDT::GetRecordCountOfDescriptors, mstv.iisdb_ldt_getrecordcountofdescriptors
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
 - IISDB_LDT::GetRecordCountOfDescriptors
 - dvbsiparser/IISDB_LDT::GetRecordCountOfDescriptors
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
 - IISDB_LDT.GetRecordCountOfDescriptors
---

# IISDB_LDT::GetRecordCountOfDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns the number of descriptors for a record in
  an Integrated Services Digital Broadcasting 
  (ISDB) linked description table (LDT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a> method to get the number of records in the LDT.

### -param pdwVal [out]

 Receives the number of descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a>