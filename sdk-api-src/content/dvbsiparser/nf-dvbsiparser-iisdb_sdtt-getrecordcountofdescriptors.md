---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordCountOfDescriptors
title: IISDB_SDTT::GetRecordCountOfDescriptors (dvbsiparser.h)
description: Returns the number of descriptors for a record in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IISDB_SDTT.GetRecordCountOfDescriptors","IISDB_SDTT::GetRecordCountOfDescriptors","dvbsiparser/IISDB_SDTT::GetRecordCountOfDescriptors","mstv.iisdb_sdtt_getrecordcountofdescriptors"]
old-location: mstv\iisdb_sdtt_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 04f32111-4c4b-4f5b-81d1-fa7c19841cd8
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IISDB_SDTT.GetRecordCountOfDescriptors, IISDB_SDTT::GetRecordCountOfDescriptors, dvbsiparser/IISDB_SDTT::GetRecordCountOfDescriptors, mstv.iisdb_sdtt_getrecordcountofdescriptors
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
 - IISDB_SDTT::GetRecordCountOfDescriptors
 - dvbsiparser/IISDB_SDTT::GetRecordCountOfDescriptors
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
 - IISDB_SDTT.GetRecordCountOfDescriptors
---

# IISDB_SDTT::GetRecordCountOfDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns the number of descriptors for a record in
  an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
      indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a> method to get the number of records in the SDTT.

### -param pdwVal [out]

Receives the number of descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>