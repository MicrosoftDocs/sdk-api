---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordVersionIndicator
title: IISDB_SDTT::GetRecordVersionIndicator
author: windows-sdk-content
description: Receives the version indicator from a record in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getrecordversionindicator.htm
tech.root: MSTV
ms.assetid: 3b4b4b4b-84b3-4181-bc84-389e72b66053
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRecordVersionIndicator, GetRecordVersionIndicator method [Microsoft TV Technologies], GetRecordVersionIndicator method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordVersionIndicator method, IISDB_SDTT.GetRecordVersionIndicator, IISDB_SDTT::GetRecordVersionIndicator, dvbsiparser/IISDB_SDTT::GetRecordVersionIndicator, mstv.iisdb_sdtt_getrecordversionindicator
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
 - IISDB_SDTT.GetRecordVersionIndicator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_SDTT::GetRecordVersionIndicator


## -description


Receives the version indicator from a record
  in an Integrated Services Digital Broadcasting
  (ISDB)  software download
  trigger table
  (SDTT). 


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a> method to get the number of records in the SDTT.



### -param pbVal [out]

Receives the version indicator.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
 

 

