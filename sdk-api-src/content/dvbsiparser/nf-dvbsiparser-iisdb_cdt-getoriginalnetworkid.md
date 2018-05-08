---
UID: NF:dvbsiparser.IISDB_CDT.GetOriginalNetworkId
title: IISDB_CDT::GetOriginalNetworkId
author: windows-driver-content
description: Gets an identifier that identifies the broadcaster that originated the MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
old-location: mstv\iisdb_cdt_getoriginalnetworkid.htm
old-project: mstv
ms.assetid: 67adf536-1163-45e3-893c-e9501fefafe7
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetOriginalNetworkId, GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetOriginalNetworkId method, IISDB_CDT.GetOriginalNetworkId, IISDB_CDT::GetOriginalNetworkId, dvbsiparser/IISDB_CDT::GetOriginalNetworkId, mstv.iisdb_cdt_getoriginalnetworkid
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
-	IISDB_CDT.GetOriginalNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_CDT::GetOriginalNetworkId


## -description



  Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT). 


## -parameters




### -param pwVal [out]


 Receives the original network ID.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>
 

 

