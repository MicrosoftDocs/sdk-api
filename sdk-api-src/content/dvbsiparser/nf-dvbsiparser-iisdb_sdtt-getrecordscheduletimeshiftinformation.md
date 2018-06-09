---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordScheduleTimeShiftInformation
title: IISDB_SDTT::GetRecordScheduleTimeShiftInformation
author: windows-sdk-content
description: Receives event time shift information from a schedule record in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getrecordscheduletimeshiftinformation.htm
old-project: mstv
ms.assetid: caf9f0b1-5529-4e8e-ab03-45d7d3268113
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordScheduleTimeShiftInformation, GetRecordScheduleTimeShiftInformation method [Microsoft TV Technologies], GetRecordScheduleTimeShiftInformation method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordScheduleTimeShiftInformation method, IISDB_SDTT.GetRecordScheduleTimeShiftInformation, IISDB_SDTT::GetRecordScheduleTimeShiftInformation, dvbsiparser/IISDB_SDTT::GetRecordScheduleTimeShiftInformation, mstv.iisdb_sdtt_getrecordscheduletimeshiftinformation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_SDTT.GetRecordScheduleTimeShiftInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::GetRecordScheduleTimeShiftInformation


## -description



  Receives event time shift information from a schedule record in
    an Integrated Services Digital Broadcasting (ISDB)  software download
  trigger table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]


  Specifies the record number,
  indexed from zero. <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
  method to get the number of records in the SDTT.



### -param pbVal [out]

Receives the event time shift data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="iisdb_sdtt::getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>
 

 

