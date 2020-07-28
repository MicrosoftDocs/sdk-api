---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordDownloadLevel
title: IISDB_SDTT::GetRecordDownloadLevel (dvbsiparser.h)
description: Gets the download level from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetRecordDownloadLevel","GetRecordDownloadLevel method [Microsoft TV Technologies]","GetRecordDownloadLevel method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetRecordDownloadLevel method","IISDB_SDTT.GetRecordDownloadLevel","IISDB_SDTT::GetRecordDownloadLevel","dvbsiparser/IISDB_SDTT::GetRecordDownloadLevel","mstv.iisdb_sdtt_getrecorddownloadlevel"]
old-location: mstv\iisdb_sdtt_getrecorddownloadlevel.htm
tech.root: mstv
ms.assetid: 22903a8d-effc-422b-bca2-907b19703b6d
ms.date: 12/05/2018
ms.keywords: GetRecordDownloadLevel, GetRecordDownloadLevel method [Microsoft TV Technologies], GetRecordDownloadLevel method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordDownloadLevel method, IISDB_SDTT.GetRecordDownloadLevel, IISDB_SDTT::GetRecordDownloadLevel, dvbsiparser/IISDB_SDTT::GetRecordDownloadLevel, mstv.iisdb_sdtt_getrecorddownloadlevel
f1_keywords:
- dvbsiparser/IISDB_SDTT.GetRecordDownloadLevel
dev_langs:
- c++
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
- IISDB_SDTT.GetRecordDownloadLevel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_SDTT::GetRecordDownloadLevel


## -description


Gets the download level from an Integrated Services Digital Broadcasting (ISDB)  software download
  trigger table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>method to get the number of records in the SDTT.



### -param pbVal [out]

Receives the download level.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>
 

 

