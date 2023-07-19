---
UID: NF:dvbsiparser.IISDB_BIT.GetOriginalNetworkId
title: IISDB_BIT::GetOriginalNetworkId (dvbsiparser.h)
description: Gets an identifier that identifies the broadcaster that originated the MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetOriginalNetworkId","GetOriginalNetworkId method [Microsoft TV Technologies]","GetOriginalNetworkId method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetOriginalNetworkId method","IISDB_BIT.GetOriginalNetworkId","IISDB_BIT::GetOriginalNetworkId","dvbsiparser/IISDB_BIT::GetOriginalNetworkId","mstv.iisdb_bit_getoriginalnetworkid"]
old-location: mstv\iisdb_bit_getoriginalnetworkid.htm
tech.root: mstv
ms.assetid: eb10f0a9-d673-46eb-bde1-3f22c518b05d
ms.date: 12/05/2018
ms.keywords: GetOriginalNetworkId, GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetOriginalNetworkId method, IISDB_BIT.GetOriginalNetworkId, IISDB_BIT::GetOriginalNetworkId, dvbsiparser/IISDB_BIT::GetOriginalNetworkId, mstv.iisdb_bit_getoriginalnetworkid
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
 - IISDB_BIT::GetOriginalNetworkId
 - dvbsiparser/IISDB_BIT::GetOriginalNetworkId
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
 - IISDB_BIT.GetOriginalNetworkId
---

# IISDB_BIT::GetOriginalNetworkId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT).

## -parameters

### -param pwVal [out]

Receives the original network ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>