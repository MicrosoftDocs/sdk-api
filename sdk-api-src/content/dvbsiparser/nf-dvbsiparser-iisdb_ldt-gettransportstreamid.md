---
UID: NF:dvbsiparser.IISDB_LDT.GetTransportStreamId
title: IISDB_LDT::GetTransportStreamId
author: windows-sdk-content
description: Returns the transport stream identifier (TSID) for an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
old-location: mstv\iisdb_ldt_gettransportstreamid.htm
old-project: mstv
ms.assetid: 382dc27b-7010-4d05-a401-ded8e0a8c932
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetTransportStreamId method, IISDB_LDT.GetTransportStreamId, IISDB_LDT::GetTransportStreamId, dvbsiparser/IISDB_LDT::GetTransportStreamId, mstv.iisdb_ldt_gettransportstreamid
ms.prod: windows
ms.technology: windows-sdk
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
 - IISDB_LDT.GetTransportStreamId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_LDT::GetTransportStreamId


## -description


Returns the transport stream identifier (TSID) for
  an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). 


## -parameters




### -param pwVal [out]

Receives the transport_stream_id field.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>
 

 

