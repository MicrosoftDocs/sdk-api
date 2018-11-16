---
UID: NF:dvbsiparser.IISDB_SDTT.GetRecordCountOfDescriptors
title: IISDB_SDTT::GetRecordCountOfDescriptors
author: windows-sdk-content
description: Returns the number of descriptors for a record in an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 04f32111-4c4b-4f5b-81d1-fa7c19841cd8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IISDB_SDTT.GetRecordCountOfDescriptors, IISDB_SDTT::GetRecordCountOfDescriptors, dvbsiparser/IISDB_SDTT::GetRecordCountOfDescriptors, mstv.iisdb_sdtt_getrecordcountofdescriptors
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
 - IISDB_SDTT.GetRecordCountOfDescriptors
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
- IISDB_SDTT.GetRecordCountOfDescriptors
: 
---

# IISDB_SDTT::GetRecordCountOfDescriptors


## -description


Returns the number of descriptors for a record in
  an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).


## -parameters




### -param dwRecordIndex [in]

Specifies the record number,
      indexed from zero. Call the <a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>method to get the number of records in the SDTT.
   


### -param pdwVal [out]

Receives the number of descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">IISDB_SDTT::GetCountOfRecords</a>
 

 

