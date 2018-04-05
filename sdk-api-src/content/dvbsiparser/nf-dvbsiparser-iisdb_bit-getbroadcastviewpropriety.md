---
UID: NF:dvbsiparser.IISDB_BIT.GetBroadcastViewPropriety
title: IISDB_BIT::GetBroadcastViewPropriety method
author: windows-driver-content
description: Returns the broadcast_view_propriety flag from a record in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_getbroadcastviewpropriety.htm
old-project: mstv
ms.assetid: b0b38631-9b0c-4ebe-9cf5-6e5847261136
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetBroadcastViewPropriety method [Microsoft TV Technologies], GetBroadcastViewPropriety method [Microsoft TV Technologies], IISDB_BIT interface, GetBroadcastViewPropriety,IISDB_BIT.GetBroadcastViewPropriety, IISDB_BIT, IISDB_BIT interface [Microsoft TV Technologies], GetBroadcastViewPropriety method, IISDB_BIT::GetBroadcastViewPropriety, dvbsiparser/IISDB_BIT::GetBroadcastViewPropriety, mstv.iisdb_bit_getbroadcastviewpropriety
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_BIT.GetBroadcastViewPropriety
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_BIT::GetBroadcastViewPropriety method


## -description



  Returns the broadcast_view_propriety flag from a record in
  an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT). The broadcast_view_propriety flag indicates whether the content associated with the broadcaster unit is appropriate for the age-based category of user.


## -parameters




### -param pbVal [out]

Receives the broadcast_view_propriety flag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

