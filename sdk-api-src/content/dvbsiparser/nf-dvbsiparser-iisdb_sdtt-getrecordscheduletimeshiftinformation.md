---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordScheduleTimeShiftInformation
title: IISDB_SDTT::GetRecordScheduleTimeShiftInformation (dvbsiparser.h)
description: Receives event time shift information from a schedule record in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetRecordScheduleTimeShiftInformation","GetRecordScheduleTimeShiftInformation method [Microsoft TV Technologies]","GetRecordScheduleTimeShiftInformation method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetRecordScheduleTimeShiftInformation method","IISDB_SDTT.GetRecordScheduleTimeShiftInformation","IISDB_SDTT::GetRecordScheduleTimeShiftInformation","dvbsiparser/IISDB_SDTT::GetRecordScheduleTimeShiftInformation","mstv.iisdb_sdtt_getrecordscheduletimeshiftinformation"]
old-location: mstv\iisdb_sdtt_getrecordscheduletimeshiftinformation.htm
tech.root: mstv
ms.assetid: caf9f0b1-5529-4e8e-ab03-45d7d3268113
ms.date: 12/05/2018
ms.keywords: GetRecordScheduleTimeShiftInformation, GetRecordScheduleTimeShiftInformation method [Microsoft TV Technologies], GetRecordScheduleTimeShiftInformation method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordScheduleTimeShiftInformation method, IISDB_SDTT.GetRecordScheduleTimeShiftInformation, IISDB_SDTT::GetRecordScheduleTimeShiftInformation, dvbsiparser/IISDB_SDTT::GetRecordScheduleTimeShiftInformation, mstv.iisdb_sdtt_getrecordscheduletimeshiftinformation
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
 - IISDB_SDTT::GetRecordScheduleTimeShiftInformation
 - dvbsiparser/IISDB_SDTT::GetRecordScheduleTimeShiftInformation
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
 - IISDB_SDTT.GetRecordScheduleTimeShiftInformation
---

# IISDB_SDTT::GetRecordScheduleTimeShiftInformation


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives event time shift information from a schedule record in
    an Integrated Services Digital Broadcasting (ISDB)  software download
  trigger table
  (SDTT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a> method to get the number of records in the SDTT.

### -param pbVal [out]

Receives the event time shift data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>