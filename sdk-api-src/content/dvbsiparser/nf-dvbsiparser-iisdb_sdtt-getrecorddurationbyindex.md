---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordDurationByIndex
title: IISDB_SDTT::GetRecordDurationByIndex method
author: windows-driver-content
description: Receives the event duration from a schedule record in an Integrated Services Digital Broadcasting (ISDB) Software Download Trigger Table (SDTT).
old-location: mstv\iisdb_sdtt_getrecorddurationbyindex.htm
old-project: mstv
ms.assetid: e7021a9e-4266-4c17-8874-4b10cf7d6428
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordDurationByIndex method [Microsoft TV Technologies], GetRecordDurationByIndex method [Microsoft TV Technologies], IISDB_SDTT interface, GetRecordDurationByIndex,IISDB_SDTT.GetRecordDurationByIndex, IISDB_SDTT, IISDB_SDTT interface [Microsoft TV Technologies], GetRecordDurationByIndex method, IISDB_SDTT::GetRecordDurationByIndex, dvbsiparser/IISDB_SDTT::GetRecordDurationByIndex, mstv.iisdb_sdtt_getrecorddurationbyindex
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IISDB_SDTT.GetRecordDurationByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::GetRecordDurationByIndex method


## -description



  Receives the event duration from a schedule record
  in an Integrated Services Digital Broadcasting
  (ISDB)  Software Download
  Trigger Table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]


  Specifies the record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
  method to get the number of records in the SDTT.



### -param dwIndex [in]


  Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/04f32111-4c4b-4f5b-81d1-fa7c19841cd8">IISDB_SDTT::GetRecordCountOfDescriptors</a> method to get the number
  of descriptors for a particular record.



### -param pmdVal [out]

Receives the record duration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
 

 

