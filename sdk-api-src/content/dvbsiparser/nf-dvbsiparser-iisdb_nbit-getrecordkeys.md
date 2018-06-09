---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordKeys
title: IISDB_NBIT::GetRecordKeys
author: windows-sdk-content
description: Gets the number_of_keys field from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_getrecordkeys.htm
old-project: mstv
ms.assetid: c8f58c17-b3b1-4fc8-b6e0-2ab23681280d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordKeys, GetRecordKeys method [Microsoft TV Technologies], GetRecordKeys method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordKeys method, IISDB_NBIT.GetRecordKeys, IISDB_NBIT::GetRecordKeys, dvbsiparser/IISDB_NBIT::GetRecordKeys, mstv.iisdb_nbit_getrecordkeys
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
 - IISDB_NBIT.GetRecordKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_NBIT::GetRecordKeys


## -description



  Gets the number_of_keys field from a record in an Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).
  


## -parameters




### -param dwRecordIndex [in]


    Specifies the record number, indexed from zero.
    Call the <a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a> method to get the number
    of records in the NBIT.
  


### -param pbKeys [out]

Gets the number_of_keys field from the NBIT record.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>



<a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a>
 

 

