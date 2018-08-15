---
UID: NF:dvbsiparser.IISDB_CDT.GetVersionHash
title: IISDB_CDT::GetVersionHash
author: windows-sdk-content
description: Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
old-location: mstv\iisdb_cdt_getversionhash.htm
old-project: mstv
ms.assetid: b6c3dd34-8db5-45a4-9c13-7e05d94c58b7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetVersionHash, GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetVersionHash method, IISDB_CDT.GetVersionHash, IISDB_CDT::GetVersionHash, dvbsiparser/IISDB_CDT::GetVersionHash, mstv.iisdb_cdt_getversionhash
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.redist: 
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
 - IISDB_CDT.GetVersionHash
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_CDT::GetVersionHash


## -description


Returns a hash value for this instance of an Integrated Services 

Digital Broadcasting (ISDB) common data table (CDT).
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




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>
 

 

