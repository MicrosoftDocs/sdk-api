---
UID: NF:dvbsiparser.IISDB_LDT.GetVersionHash
title: IISDB_LDT::GetVersionHash (dvbsiparser.h)
author: windows-sdk-content
description: Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
old-location: mstv\iisdb_ldt_getversionhash.htm
tech.root: mstv
ms.assetid: ea7f027c-60c3-4dcd-963b-37ae6b088c81
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersionHash, GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetVersionHash method, IISDB_LDT.GetVersionHash, IISDB_LDT::GetVersionHash, dvbsiparser/IISDB_LDT::GetVersionHash, mstv.iisdb_ldt_getversionhash
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
 - IISDB_LDT.GetVersionHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_LDT::GetVersionHash


## -description


Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). Tables that refer to
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




<a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>
 

 

