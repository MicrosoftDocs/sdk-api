---
UID: NF:dvbsiparser.IISDB_LDT.GetTransportStreamId
title: IISDB_LDT::GetTransportStreamId (dvbsiparser.h)
description: Returns the transport stream identifier (TSID) for an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).helpviewer_keywords: ["GetTransportStreamId","GetTransportStreamId method [Microsoft TV Technologies]","GetTransportStreamId method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetTransportStreamId method","IISDB_LDT.GetTransportStreamId","IISDB_LDT::GetTransportStreamId","dvbsiparser/IISDB_LDT::GetTransportStreamId","mstv.iisdb_ldt_gettransportstreamid"]
old-location: mstv\iisdb_ldt_gettransportstreamid.htm
tech.root: mstv
ms.assetid: 382dc27b-7010-4d05-a401-ded8e0a8c932
ms.date: 12/05/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetTransportStreamId method, IISDB_LDT.GetTransportStreamId, IISDB_LDT::GetTransportStreamId, dvbsiparser/IISDB_LDT::GetTransportStreamId, mstv.iisdb_ldt_gettransportstreamid
f1_keywords:
- dvbsiparser/IISDB_LDT.GetTransportStreamId
dev_langs:
- c++
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
- IISDB_LDT.GetTransportStreamId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>
 

 

