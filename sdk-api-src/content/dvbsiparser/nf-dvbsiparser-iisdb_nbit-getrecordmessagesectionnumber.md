---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordMessageSectionNumber
title: IISDB_NBIT::GetRecordMessageSectionNumber (dvbsiparser.h)
description: Gets the section_number field from a record in Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetRecordMessageSectionNumber","GetRecordMessageSectionNumber method [Microsoft TV Technologies]","GetRecordMessageSectionNumber method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordMessageSectionNumber method","IISDB_NBIT.GetRecordMessageSectionNumber","IISDB_NBIT::GetRecordMessageSectionNumber","dvbsiparser/IISDB_NBIT::GetRecordMessageSectionNumber","mstv.iisdb_nbit_getrecordmessagesectionnumber"]
old-location: mstv\iisdb_nbit_getrecordmessagesectionnumber.htm
tech.root: mstv
ms.assetid: 3bfab381-f5af-4583-b268-72c83f3bfb8d
ms.date: 12/05/2018
ms.keywords: GetRecordMessageSectionNumber, GetRecordMessageSectionNumber method [Microsoft TV Technologies], GetRecordMessageSectionNumber method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordMessageSectionNumber method, IISDB_NBIT.GetRecordMessageSectionNumber, IISDB_NBIT::GetRecordMessageSectionNumber, dvbsiparser/IISDB_NBIT::GetRecordMessageSectionNumber, mstv.iisdb_nbit_getrecordmessagesectionnumber
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
 - IISDB_NBIT::GetRecordMessageSectionNumber
 - dvbsiparser/IISDB_NBIT::GetRecordMessageSectionNumber
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
 - IISDB_NBIT.GetRecordMessageSectionNumber
---

# IISDB_NBIT::GetRecordMessageSectionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the section_number field from a record in  Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).
  The section_ number field identifies the section so that
  the demultiplexer can successfully reconstruct the sections in their original order.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a> method to get the number
  of records in the NBIT.

### -param pbVal [out]

Gets the section_number field value from the NBIT record.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a>