---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordStartTimeByIndex
title: IISDB_SDTT::GetRecordStartTimeByIndex
author: windows-sdk-content
description: Gets an event start time from a schedule record in in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getrecordstarttimebyindex.htm
old-project: mstv
ms.assetid: ccbeb664-6c84-4f50-9376-dfa0492aa9e1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordStartTimeByIndex, GetRecordStartTimeByIndex method [Microsoft TV Technologies], GetRecordStartTimeByIndex method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordStartTimeByIndex method, IISDB_SDTT.GetRecordStartTimeByIndex, IISDB_SDTT::GetRecordStartTimeByIndex, dvbsiparser/IISDB_SDTT::GetRecordStartTimeByIndex, mstv.iisdb_sdtt_getrecordstarttimebyindex
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_SDTT.GetRecordStartTimeByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::GetRecordStartTimeByIndex


## -description



  Gets an event start time from a schedule record in
  in an Integrated Services Digital Broadcasting
  (ISDB)  software download
  trigger table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]


  Specifies the record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
  method to get the number of records in the SDTT.



### -param dwIndex [in]

Index to the schedules for the selected content.


### -param pmdtVal [out]

Receives the event start time.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
 

 

