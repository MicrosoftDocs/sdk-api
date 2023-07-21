---
UID: NF:dvbsiparser.IISDB_SDTT.GetCountOfRecords
title: IISDB_SDTT::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetCountOfRecords method","IISDB_SDTT.GetCountOfRecords","IISDB_SDTT::GetCountOfRecords","dvbsiparser/IISDB_SDTT::GetCountOfRecords","mstv.iisdb_sdtt_getcountofrecords"]
old-location: mstv\iisdb_sdtt_getcountofrecords.htm
tech.root: mstv
ms.assetid: 3e445eed-907c-4a9b-80b7-b16460bc131c
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetCountOfRecords method, IISDB_SDTT.GetCountOfRecords, IISDB_SDTT::GetCountOfRecords, dvbsiparser/IISDB_SDTT::GetCountOfRecords, mstv.iisdb_sdtt_getcountofrecords
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
 - IISDB_SDTT::GetCountOfRecords
 - dvbsiparser/IISDB_SDTT::GetCountOfRecords
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
 - IISDB_SDTT.GetCountOfRecords
---

# IISDB_SDTT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in an
   Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).

## -parameters

### -param pdwVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>