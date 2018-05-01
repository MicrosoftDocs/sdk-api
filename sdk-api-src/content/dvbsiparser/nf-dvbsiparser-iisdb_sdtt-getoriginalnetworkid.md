---
UID: NF:dvbsiparser.IISDB_SDTT.GetOriginalNetworkId
title: IISDB_SDTT::GetOriginalNetworkId method
author: windows-driver-content
description: Gets an identifier that identifies the broadcaster that originated the MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getoriginalnetworkid.htm
old-project: mstv
ms.assetid: 49368eaf-3115-4fdf-ac7a-39459d199ce0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies], IISDB_SDTT interface, GetOriginalNetworkId,IISDB_SDTT.GetOriginalNetworkId, IISDB_SDTT, IISDB_SDTT interface [Microsoft TV Technologies], GetOriginalNetworkId method, IISDB_SDTT::GetOriginalNetworkId, dvbsiparser/IISDB_SDTT::GetOriginalNetworkId, mstv.iisdb_sdtt_getoriginalnetworkid
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
-	IISDB_SDTT.GetOriginalNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::GetOriginalNetworkId method


## -description



  Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an Integrated Services Digital Broadcasting 
  (ISDB) software download
  trigger table
  (SDTT).


## -parameters




### -param pwVal [out]

Receives the original network ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>
 

 

