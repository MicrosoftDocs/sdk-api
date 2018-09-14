---
UID: NF:dvbsiparser.IISDB_BIT.GetRecordCountOfDescriptors
title: IISDB_BIT::GetRecordCountOfDescriptors
author: windows-sdk-content
description: Returns the number of descriptors for subtables in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_getrecordcountofdescriptors.htm
tech.root: MSTV
ms.assetid: 08df6f74-dbeb-4d32-8b0f-4ec88d35ff36
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IISDB_BIT.GetRecordCountOfDescriptors, IISDB_BIT::GetRecordCountOfDescriptors, dvbsiparser/IISDB_BIT::GetRecordCountOfDescriptors, mstv.iisdb_bit_getrecordcountofdescriptors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IISDB_BIT.GetRecordCountOfDescriptors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_BIT::GetRecordCountOfDescriptors


## -description


Returns the number of descriptors for subtables in
  an Integrated Services Digital Broadcasting (ISDB)
  broadcaster information table (BIT).


## -parameters




### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/3f36c03a-462e-479a-ad8c-5322377dbca0">IISDB_BIT::GetCountOfRecords</a> 

  method to get the number of records in the BIT.


### -param pdwVal [out]

Receives the number of descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

