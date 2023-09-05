---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordStartTimeByIndex
title: IISDB_SDTT::GetRecordStartTimeByIndex (dvbsiparser.h)
description: Gets an event start time from a schedule record in in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetRecordStartTimeByIndex","GetRecordStartTimeByIndex method [Microsoft TV Technologies]","GetRecordStartTimeByIndex method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetRecordStartTimeByIndex method","IISDB_SDTT.GetRecordStartTimeByIndex","IISDB_SDTT::GetRecordStartTimeByIndex","dvbsiparser/IISDB_SDTT::GetRecordStartTimeByIndex","mstv.iisdb_sdtt_getrecordstarttimebyindex"]
old-location: mstv\iisdb_sdtt_getrecordstarttimebyindex.htm
tech.root: mstv
ms.assetid: ccbeb664-6c84-4f50-9376-dfa0492aa9e1
ms.date: 12/05/2018
ms.keywords: GetRecordStartTimeByIndex, GetRecordStartTimeByIndex method [Microsoft TV Technologies], GetRecordStartTimeByIndex method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordStartTimeByIndex method, IISDB_SDTT.GetRecordStartTimeByIndex, IISDB_SDTT::GetRecordStartTimeByIndex, dvbsiparser/IISDB_SDTT::GetRecordStartTimeByIndex, mstv.iisdb_sdtt_getrecordstarttimebyindex
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
 - IISDB_SDTT::GetRecordStartTimeByIndex
 - dvbsiparser/IISDB_SDTT::GetRecordStartTimeByIndex
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
 - IISDB_SDTT.GetRecordStartTimeByIndex
---

# IISDB_SDTT::GetRecordStartTimeByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an event start time from a schedule record in
  in an Integrated Services Digital Broadcasting
  (ISDB)  software download
  trigger table
  (SDTT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a> method to get the number of records in the SDTT.

### -param dwIndex [in]

Index to the schedules for the selected content.

### -param pmdtVal [out]

Receives the event start time.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>