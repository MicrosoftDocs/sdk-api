---
UID: NF:dvbsiparser.IISDB_BIT.GetRecordDescriptorByTag
title: IISDB_BIT::GetRecordDescriptorByTag (dvbsiparser.h)
description: Searches a record in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetRecordDescriptorByTag","GetRecordDescriptorByTag method [Microsoft TV Technologies]","GetRecordDescriptorByTag method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetRecordDescriptorByTag method","IISDB_BIT.GetRecordDescriptorByTag","IISDB_BIT::GetRecordDescriptorByTag","dvbsiparser/IISDB_BIT::GetRecordDescriptorByTag","mstv.iisdb_bit_getrecorddescriptorbytag"]
old-location: mstv\iisdb_bit_getrecorddescriptorbytag.htm
tech.root: mstv
ms.assetid: 9e22da6e-1721-46c5-9a98-7d21edaa6d14
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IISDB_BIT.GetRecordDescriptorByTag, IISDB_BIT::GetRecordDescriptorByTag, dvbsiparser/IISDB_BIT::GetRecordDescriptorByTag, mstv.iisdb_bit_getrecorddescriptorbytag
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
 - IISDB_BIT::GetRecordDescriptorByTag
 - dvbsiparser/IISDB_BIT::GetRecordDescriptorByTag
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
 - IISDB_BIT.GetRecordDescriptorByTag
---

# IISDB_BIT::GetRecordDescriptorByTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Searches a record in
  an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a> method to get the number of records in the BIT.

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

Address of a variable that receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor
  </a> interface pointer. Use this interface to retrieve the information
  in the descriptor. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor
  </a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a>