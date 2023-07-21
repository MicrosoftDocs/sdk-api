---
UID: NF:dvbsiparser.IISDB_LDT.GetOriginalNetworkId
title: IISDB_LDT::GetOriginalNetworkId (dvbsiparser.h)
description: Gets an identifier that identifies the broadcaster that originated the MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
helpviewer_keywords: ["GetOriginalNetworkId","GetOriginalNetworkId method [Microsoft TV Technologies]","GetOriginalNetworkId method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetOriginalNetworkId method","IISDB_LDT.GetOriginalNetworkId","IISDB_LDT::GetOriginalNetworkId","dvbsiparser/IISDB_LDT::GetOriginalNetworkId","mstv.iisdb_ldt_getoriginalnetworkid"]
old-location: mstv\iisdb_ldt_getoriginalnetworkid.htm
tech.root: mstv
ms.assetid: a887536d-7ccb-4c28-8ea7-ded90683c036
ms.date: 12/05/2018
ms.keywords: GetOriginalNetworkId, GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetOriginalNetworkId method, IISDB_LDT.GetOriginalNetworkId, IISDB_LDT::GetOriginalNetworkId, dvbsiparser/IISDB_LDT::GetOriginalNetworkId, mstv.iisdb_ldt_getoriginalnetworkid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IISDB_LDT::GetOriginalNetworkId
 - dvbsiparser/IISDB_LDT::GetOriginalNetworkId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_LDT.GetOriginalNetworkId
---

# IISDB_LDT::GetOriginalNetworkId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an Integrated Services Digital Broadcasting 
  (ISDB) linked description table (LDT).

## -parameters

### -param pwVal [out]

Receives the original network ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>