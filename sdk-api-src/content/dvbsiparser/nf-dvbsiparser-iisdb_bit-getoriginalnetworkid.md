---
UID: NF:dvbsiparser.IISDB_BIT.GetOriginalNetworkId
title: IISDB_BIT::GetOriginalNetworkId method
author: windows-driver-content
description: Gets an identifier that identifies the broadcaster that originated the MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_getoriginalnetworkid.htm
old-project: mstv
ms.assetid: eb10f0a9-d673-46eb-bde1-3f22c518b05d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies], IISDB_BIT interface, GetOriginalNetworkId,IISDB_BIT.GetOriginalNetworkId, IISDB_BIT, IISDB_BIT interface [Microsoft TV Technologies], GetOriginalNetworkId method, IISDB_BIT::GetOriginalNetworkId, dvbsiparser/IISDB_BIT::GetOriginalNetworkId, mstv.iisdb_bit_getoriginalnetworkid
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
-	IISDB_BIT.GetOriginalNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_BIT::GetOriginalNetworkId method


## -description



  Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT). 


## -parameters




### -param pwVal [out]

Receives the original network ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

