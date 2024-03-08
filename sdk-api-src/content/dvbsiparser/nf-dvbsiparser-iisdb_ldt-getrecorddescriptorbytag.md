---
UID: NF:dvbsiparser.IISDB_LDT.GetRecordDescriptorByTag
title: IISDB_LDT::GetRecordDescriptorByTag (dvbsiparser.h)
description: Searches a record in an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT) for a specific descriptor tag.
helpviewer_keywords: ["GetRecordDescriptorByTag","GetRecordDescriptorByTag method [Microsoft TV Technologies]","GetRecordDescriptorByTag method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetRecordDescriptorByTag method","IISDB_LDT.GetRecordDescriptorByTag","IISDB_LDT::GetRecordDescriptorByTag","dvbsiparser/IISDB_LDT::GetRecordDescriptorByTag","mstv.iisdb_ldt_getrecorddescriptorbytag"]
old-location: mstv\iisdb_ldt_getrecorddescriptorbytag.htm
tech.root: mstv
ms.assetid: 6d1fc08c-9c5b-4361-a144-d8b423250c51
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IISDB_LDT.GetRecordDescriptorByTag, IISDB_LDT::GetRecordDescriptorByTag, dvbsiparser/IISDB_LDT::GetRecordDescriptorByTag, mstv.iisdb_ldt_getrecorddescriptorbytag
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
 - IISDB_LDT::GetRecordDescriptorByTag
 - dvbsiparser/IISDB_LDT::GetRecordDescriptorByTag
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
 - IISDB_LDT.GetRecordDescriptorByTag
---

# IISDB_LDT::GetRecordDescriptorByTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Searches a record in
  an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT) for a specific descriptor tag.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a> method to get the number of records in the LDT.

### -param bTag [in]

Specifies the descriptor tag for which to search.

### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position
  in the descriptor list. This parameter is optional.
  If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the
  first descriptor in the list. Otherwise, the search starts from
  the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor,
  if any. You can use this parameter to iterate through the descriptor list,
  looking for every instance of a particular descriptor tag.

### -param ppDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface of the object that contains the LDT. Use this interface to retrieve the information
  in the descriptor. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a>