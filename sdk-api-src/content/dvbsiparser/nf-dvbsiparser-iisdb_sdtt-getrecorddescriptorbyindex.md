---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordDescriptorByIndex
title: IISDB_SDTT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: Returns a descriptor for a specified record in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IISDB_SDTT.GetRecordDescriptorByIndex","IISDB_SDTT::GetRecordDescriptorByIndex","dvbsiparser/IISDB_SDTT::GetRecordDescriptorByIndex","mstv.iisdb_sdtt_getrecorddescriptorbyindex"]
old-location: mstv\iisdb_sdtt_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: c8aab681-4858-4ad2-84a7-15a9b8310d6f
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IISDB_SDTT.GetRecordDescriptorByIndex, IISDB_SDTT::GetRecordDescriptorByIndex, dvbsiparser/IISDB_SDTT::GetRecordDescriptorByIndex, mstv.iisdb_sdtt_getrecorddescriptorbyindex
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
 - IISDB_SDTT::GetRecordDescriptorByIndex
 - dvbsiparser/IISDB_SDTT::GetRecordDescriptorByIndex
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
 - IISDB_SDTT.GetRecordDescriptorByIndex
---

# IISDB_SDTT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns a descriptor for a specified record
  in an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a> method to get the number
  of records in the SDTT.

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordcountofdescriptors">IISDB_SDTT::GetRecordCountOfDescriptors</a> method to get the number
  of descriptors for a particular record.

### -param ppDescriptor [out]

Pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface for the descriptor being retrieved. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordcountofdescriptors">IISDB_SDTT::GetRecordCountOfDescriptors</a>