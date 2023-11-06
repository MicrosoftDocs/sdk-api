---
UID: NF:dvbsiparser.IISDB_LDT.GetRecordDescriptorByIndex
title: IISDB_LDT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: Returns a descriptor for a specified record in an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IISDB_LDT.GetRecordDescriptorByIndex","IISDB_LDT::GetRecordDescriptorByIndex","dvbsiparser/IISDB_LDT::GetRecordDescriptorByIndex","mstv.iisdb_ldt_getrecorddescriptorbyindex"]
old-location: mstv\iisdb_ldt_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: a551794a-6051-4c8e-9d44-5938974a6df4
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IISDB_LDT.GetRecordDescriptorByIndex, IISDB_LDT::GetRecordDescriptorByIndex, dvbsiparser/IISDB_LDT::GetRecordDescriptorByIndex, mstv.iisdb_ldt_getrecorddescriptorbyindex
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
 - IISDB_LDT::GetRecordDescriptorByIndex
 - dvbsiparser/IISDB_LDT::GetRecordDescriptorByIndex
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
 - IISDB_LDT.GetRecordDescriptorByIndex
---

# IISDB_LDT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns a descriptor for a specified record
  in an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a> method to get the number of records in the LDT.

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero.
Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getrecordcountofdescriptors">IISDB_LDT::GetRecordCountOfDescriptors</a> method 
to get the number of descriptors for a particular record.

### -param ppDescriptor [out]

Pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface for the object that contains the LDT. Use this interface to retrieve the information in the descriptor. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getrecordcountofdescriptors">IISDB_LDT::GetRecordCountOfDescriptors</a>