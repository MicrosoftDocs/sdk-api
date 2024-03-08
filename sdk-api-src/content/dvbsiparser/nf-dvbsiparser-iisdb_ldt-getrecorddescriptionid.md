---
UID: NF:dvbsiparser.IISDB_LDT.GetRecordDescriptionId
title: IISDB_LDT::GetRecordDescriptionId (dvbsiparser.h)
description: Gets the record description ID from an Integrated services Digital Broadcasting System (IDBS) linked description table (LDT). The description ID field identifies a collected description in the LDT.
helpviewer_keywords: ["GetRecordDescriptionId","GetRecordDescriptionId method [Microsoft TV Technologies]","GetRecordDescriptionId method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetRecordDescriptionId method","IISDB_LDT.GetRecordDescriptionId","IISDB_LDT::GetRecordDescriptionId","dvbsiparser/IISDB_LDT::GetRecordDescriptionId","mstv.iisdb_ldt_getrecorddescriptionid"]
old-location: mstv\iisdb_ldt_getrecorddescriptionid.htm
tech.root: mstv
ms.assetid: 0c101068-8a33-4c65-b553-fcd5989c4bd7
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptionId, GetRecordDescriptionId method [Microsoft TV Technologies], GetRecordDescriptionId method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetRecordDescriptionId method, IISDB_LDT.GetRecordDescriptionId, IISDB_LDT::GetRecordDescriptionId, dvbsiparser/IISDB_LDT::GetRecordDescriptionId, mstv.iisdb_ldt_getrecorddescriptionid
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
 - IISDB_LDT::GetRecordDescriptionId
 - dvbsiparser/IISDB_LDT::GetRecordDescriptionId
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
 - IISDB_LDT.GetRecordDescriptionId
---

# IISDB_LDT::GetRecordDescriptionId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the record description ID from an Integrated services Digital Broadcasting System
  (IDBS) linked description table (LDT). The description ID field identifies a collected description in the LDT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a> method to get the number of records in the LDT.

### -param pwVal [out]

Receives the description_id field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">IISDB_LDT::GetCountOfRecords</a>