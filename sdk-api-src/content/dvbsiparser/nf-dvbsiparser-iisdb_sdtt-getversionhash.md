---
UID: NF:dvbsiparser.IISDB_SDTT.GetVersionHash
title: IISDB_SDTT::GetVersionHash method
author: windows-driver-content
description: Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getversionhash.htm
old-project: mstv
ms.assetid: 269b96c7-7748-44b3-9e6d-2089bcc56664
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies], IISDB_SDTT interface, GetVersionHash,IISDB_SDTT.GetVersionHash, IISDB_SDTT, IISDB_SDTT interface [Microsoft TV Technologies], GetVersionHash method, IISDB_SDTT::GetVersionHash, dvbsiparser/IISDB_SDTT::GetVersionHash, mstv.iisdb_sdtt_getversionhash
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_SDTT.GetVersionHash
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::GetVersionHash method


## -description



  Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
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




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>
 

 

