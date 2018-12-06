---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordNewVersion
title: IISDB_SDTT::GetRecordNewVersion
author: windows-sdk-content
description: Returns a new version_number field value from a subtable within an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getrecordnewversion.htm
tech.root: mstv
ms.assetid: 0a121a8b-10fd-4f78-922a-6be704c2cab4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordNewVersion, GetRecordNewVersion method [Microsoft TV Technologies], GetRecordNewVersion method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordNewVersion method, IISDB_SDTT.GetRecordNewVersion, IISDB_SDTT::GetRecordNewVersion, dvbsiparser/IISDB_SDTT::GetRecordNewVersion, mstv.iisdb_sdtt_getrecordnewversion
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
 - IISDB_SDTT.GetRecordNewVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_SDTT::GetRecordNewVersion


## -description


Returns a new version_number field value from a subtable
  within an
  Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>method to get the number of records in the SDTT.



### -param pwVal [out]

Receives the new version_number field value.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="iisdb_sdtt::getcountofrecords">IISDB_SDTT::GetCountOfRecords</a>
 

 

