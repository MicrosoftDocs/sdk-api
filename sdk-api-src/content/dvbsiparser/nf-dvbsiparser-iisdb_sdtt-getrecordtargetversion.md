---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordTargetVersion
title: IISDB_SDTT::GetRecordTargetVersion
author: windows-sdk-content
description: Receives the target version from a record in an Integrated Services Digital Broadcasting (ISDB) Software Download Trigger Table (SDTT).
old-location: mstv\iisdb_sdtt_getrecordtargetversion.htm
tech.root: mstv
ms.assetid: e8e85c5b-e577-45b9-b377-c21700c818bb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRecordTargetVersion, GetRecordTargetVersion method [Microsoft TV Technologies], GetRecordTargetVersion method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordTargetVersion method, IISDB_SDTT.GetRecordTargetVersion, IISDB_SDTT::GetRecordTargetVersion, dvbsiparser/IISDB_SDTT::GetRecordTargetVersion, mstv.iisdb_sdtt_getrecordtargetversion
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
 - IISDB_SDTT.GetRecordTargetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IISDB_SDTT.GetRecordTargetVersion
: 
---

# IISDB_SDTT::GetRecordTargetVersion


## -description


Receives the target version from a record 
  in an Integrated Services Digital Broadcasting
  (ISDB)  Software Download
  Trigger Table
  (SDTT). 


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a> method to get the number of records in the SDTT.



### -param pwVal [out]

Receives the target version.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
 

 

