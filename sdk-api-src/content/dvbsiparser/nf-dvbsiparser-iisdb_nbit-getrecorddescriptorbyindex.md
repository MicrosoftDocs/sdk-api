---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordDescriptorByIndex
title: IISDB_NBIT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: Retrieves a descriptor for a specified record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT) based on the descriptor index.
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IISDB_NBIT.GetRecordDescriptorByIndex","IISDB_NBIT::GetRecordDescriptorByIndex","dvbsiparser/IISDB_NBIT::GetRecordDescriptorByIndex","mstv.iisdb_nbit_getrecorddescriptorbyindex"]
old-location: mstv\iisdb_nbit_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: 0f7da95d-ba3f-4cdc-aea0-38abae260159
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IISDB_NBIT.GetRecordDescriptorByIndex, IISDB_NBIT::GetRecordDescriptorByIndex, dvbsiparser/IISDB_NBIT::GetRecordDescriptorByIndex, mstv.iisdb_nbit_getrecorddescriptorbyindex
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
 - IISDB_NBIT::GetRecordDescriptorByIndex
 - dvbsiparser/IISDB_NBIT::GetRecordDescriptorByIndex
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
 - IISDB_NBIT.GetRecordDescriptorByIndex
---

# IISDB_NBIT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Retrieves a descriptor for a specified record in 
  an Integrated Services Digital Broadcasting (ISDB) 
  network broadcaster information table (NBIT)
  based on the descriptor index.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. 
Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a> 
 method to get the number 
of records in the NBIT.

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. 
Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordcountofdescriptors">IISDB_NBIT::GetRecordCountOfDescriptors</a> method 
to get the number of descriptors for a particular record.

### -param ppDescriptor [out]

Pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface implemented by the descriptor. The caller is responsible for freeing the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordcountofdescriptors">IISDB_NBIT::GetRecordCountOfDescriptors</a>