---
UID: NF:dvbsiparser.IISDB_BIT.GetRecordDescriptorByIndex
title: IISDB_BIT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: Returns a descriptor for a specified record in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IISDB_BIT.GetRecordDescriptorByIndex","IISDB_BIT::GetRecordDescriptorByIndex","dvbsiparser/IISDB_BIT::GetRecordDescriptorByIndex","mstv.iisdb_bit_getrecorddescriptorbyindex"]
old-location: mstv\iisdb_bit_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: f3833ab6-39f8-499e-bd3f-f0f524a8b1d4
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IISDB_BIT.GetRecordDescriptorByIndex, IISDB_BIT::GetRecordDescriptorByIndex, dvbsiparser/IISDB_BIT::GetRecordDescriptorByIndex, mstv.iisdb_bit_getrecorddescriptorbyindex
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
 - IISDB_BIT::GetRecordDescriptorByIndex
 - dvbsiparser/IISDB_BIT::GetRecordDescriptorByIndex
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
 - IISDB_BIT.GetRecordDescriptorByIndex
---

# IISDB_BIT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns a descriptor for a specified record
  in an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a> method to get the number
  of records in the BIT.

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">IISDB_BIT::GetRecordCountOfDescriptors</a> method
  to get the number of descriptors for a particular record.

### -param ppDescriptor [out]

Pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface implemented by the descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">IISDB_BIT::GetRecordCountOfDescriptors</a>