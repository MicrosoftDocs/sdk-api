---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordInformationId
title: IISDB_NBIT::GetRecordInformationId
author: windows-sdk-content
description: an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_getrecordinformationid.htm
old-project: mstv
ms.assetid: 9535d587-3e37-4d12-9b96-66ff1c2cf6f3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordInformationId, GetRecordInformationId method [Microsoft TV Technologies], GetRecordInformationId method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordInformationId method, IISDB_NBIT.GetRecordInformationId, IISDB_NBIT::GetRecordInformationId, dvbsiparser/IISDB_NBIT::GetRecordInformationId, mstv.iisdb_nbit_getrecordinformationid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.redist: 
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
 - IISDB_NBIT.GetRecordInformationId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_NBIT::GetRecordInformationId


## -description


an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
  


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
    Call the <a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a> method to get the number
    of records in the NBIT.
  


### -param pwVal [out]

Receives the information_type field for the record.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>
 

 

