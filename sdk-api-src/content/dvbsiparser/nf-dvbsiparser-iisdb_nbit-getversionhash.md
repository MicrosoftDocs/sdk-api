---
UID: NF:dvbsiparser.IISDB_NBIT.GetVersionHash
title: IISDB_NBIT::GetVersionHash (dvbsiparser.h)
author: windows-sdk-content
description: Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_getversionhash.htm
tech.root: mstv
ms.assetid: 6de71e7e-7296-46ad-a0fa-3aadb9a24ab5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersionHash, GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetVersionHash method, IISDB_NBIT.GetVersionHash, IISDB_NBIT::GetVersionHash, dvbsiparser/IISDB_NBIT::GetVersionHash, mstv.iisdb_nbit_getversionhash
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
 - IISDB_NBIT.GetVersionHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_NBIT::GetVersionHash


## -description


Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT). Tables that refer to
  the same content
  will return the same hash value, even though the tables have different version_number and table_id fields. You can use this hash value to identify when
  two tables carry the same information,
  even if the tables are carried on different transport streams.


## -parameters




### -param pdwVersionHash [out]

Receives the hash value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>
 

 

