---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordDurationByIndex
title: IISDB_SDTT::GetRecordDurationByIndex (dvbsiparser.h)
author: windows-sdk-content
description: Receives the event duration from a schedule record in an Integrated Services Digital Broadcasting (ISDB) Software Download Trigger Table (SDTT).
old-location: mstv\iisdb_sdtt_getrecorddurationbyindex.htm
tech.root: mstv
ms.assetid: e7021a9e-4266-4c17-8874-4b10cf7d6428
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordDurationByIndex, GetRecordDurationByIndex method [Microsoft TV Technologies], GetRecordDurationByIndex method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordDurationByIndex method, IISDB_SDTT.GetRecordDurationByIndex, IISDB_SDTT::GetRecordDurationByIndex, dvbsiparser/IISDB_SDTT::GetRecordDurationByIndex, mstv.iisdb_sdtt_getrecorddurationbyindex
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_SDTT.GetRecordDurationByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_SDTT::GetRecordDurationByIndex


## -description


Receives the event duration from a schedule record
  in an Integrated Services Digital Broadcasting
  (ISDB)  Software Download
  Trigger Table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>method to get the number of records in the SDTT.



### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordcountofdescriptors">IISDB_SDTT::GetRecordCountOfDescriptors</a> method to get the number
  of descriptors for a particular record.



### -param pmdVal [out]

Receives the record duration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>
 

 

