---
UID: NF:dvbsiparser.IISDB_BIT.GetTableDescriptorByIndex
title: IISDB_BIT::GetTableDescriptorByIndex (dvbsiparser.h)
description: Returns a descriptor for a specified table in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetTableDescriptorByIndex","GetTableDescriptorByIndex method [Microsoft TV Technologies]","GetTableDescriptorByIndex method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetTableDescriptorByIndex method","IISDB_BIT.GetTableDescriptorByIndex","IISDB_BIT::GetTableDescriptorByIndex","dvbsiparser/IISDB_BIT::GetTableDescriptorByIndex","mstv.iisdb_bit_gettabledescriptorbyindex"]
old-location: mstv\iisdb_bit_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: 5c6002b2-61c3-4d0c-87b9-682c3277792c
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IISDB_BIT.GetTableDescriptorByIndex, IISDB_BIT::GetTableDescriptorByIndex, dvbsiparser/IISDB_BIT::GetTableDescriptorByIndex, mstv.iisdb_bit_gettabledescriptorbyindex
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
 - IISDB_BIT::GetTableDescriptorByIndex
 - dvbsiparser/IISDB_BIT::GetTableDescriptorByIndex
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
 - IISDB_BIT.GetTableDescriptorByIndex
---

# IISDB_BIT::GetTableDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns a descriptor for a specified table
  in an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT).

## -parameters

### -param dwIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a> method to get the number of records in the BIT.

### -param ppDescriptor [out]

Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">IISDB_BIT::GetRecordCountOfDescriptors</a> method
  to get the number of descriptors for a particular record.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">IISDB_BIT::GetRecordCountOfDescriptors</a>