---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordGroup
title: IISDB_SDTT::GetRecordGroup (dvbsiparser.h)
description: Receives the recording download level from a record in an Integrated services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetRecordGroup","GetRecordGroup method [Microsoft TV Technologies]","GetRecordGroup method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetRecordGroup method","IISDB_SDTT.GetRecordGroup","IISDB_SDTT::GetRecordGroup","dvbsiparser/IISDB_SDTT::GetRecordGroup","mstv.iisdb_sdtt_getrecordgroup"]
old-location: mstv\iisdb_sdtt_getrecordgroup.htm
tech.root: mstv
ms.assetid: 6798e477-754d-49a3-84f1-04d1a60094a7
ms.date: 12/05/2018
ms.keywords: GetRecordGroup, GetRecordGroup method [Microsoft TV Technologies], GetRecordGroup method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordGroup method, IISDB_SDTT.GetRecordGroup, IISDB_SDTT::GetRecordGroup, dvbsiparser/IISDB_SDTT::GetRecordGroup, mstv.iisdb_sdtt_getrecordgroup
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
 - IISDB_SDTT::GetRecordGroup
 - dvbsiparser/IISDB_SDTT::GetRecordGroup
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
 - IISDB_SDTT.GetRecordGroup
---

# IISDB_SDTT::GetRecordGroup


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives the recording download level from a record
  in an Integrated services Digital Broadcasting 
  (ISDB)  software download
  trigger table
  (SDTT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a> method to get the number of records in the SDTT.

### -param pbVal [out]

Receives the recording download level.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>