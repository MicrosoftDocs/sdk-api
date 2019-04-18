---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordMessageSectionNumber
title: IISDB_NBIT::GetRecordMessageSectionNumber (dvbsiparser.h)
author: windows-sdk-content
description: Gets the section_number field from a record in Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_getrecordmessagesectionnumber.htm
tech.root: mstv
ms.assetid: 3bfab381-f5af-4583-b268-72c83f3bfb8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordMessageSectionNumber, GetRecordMessageSectionNumber method [Microsoft TV Technologies], GetRecordMessageSectionNumber method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordMessageSectionNumber method, IISDB_NBIT.GetRecordMessageSectionNumber, IISDB_NBIT::GetRecordMessageSectionNumber, dvbsiparser/IISDB_NBIT::GetRecordMessageSectionNumber, mstv.iisdb_nbit_getrecordmessagesectionnumber
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
 - IISDB_NBIT.GetRecordMessageSectionNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_NBIT::GetRecordMessageSectionNumber


## -description


Gets the section_number field from a record in  Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).
  The section_ number field identifies the section so that
  the demultiplexer can successfully reconstruct the sections in their original order.



## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a> method to get the number
  of records in the NBIT.



### -param pbVal [out]

Gets the section_number field value from the NBIT record.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>



<a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a>
 

 

