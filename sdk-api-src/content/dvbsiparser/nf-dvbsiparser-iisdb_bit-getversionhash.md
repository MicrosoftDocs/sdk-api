---
UID: NF:dvbsiparser.IISDB_BIT.GetVersionHash
title: IISDB_BIT::GetVersionHash (dvbsiparser.h)
author: windows-sdk-content
description: Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_getversionhash.htm
tech.root: mstv
ms.assetid: 26423a5f-710b-405f-acf2-1aafbeb304d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersionHash, GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetVersionHash method, IISDB_BIT.GetVersionHash, IISDB_BIT::GetVersionHash, dvbsiparser/IISDB_BIT::GetVersionHash, mstv.iisdb_bit_getversionhash
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
 - IISDB_BIT.GetVersionHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_BIT::GetVersionHash


## -description


Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
  Tables that refer to
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




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

