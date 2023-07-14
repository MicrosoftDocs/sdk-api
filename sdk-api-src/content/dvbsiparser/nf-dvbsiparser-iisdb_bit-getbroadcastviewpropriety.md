---
UID: NF:dvbsiparser.IISDB_BIT.GetBroadcastViewPropriety
title: IISDB_BIT::GetBroadcastViewPropriety (dvbsiparser.h)
description: Returns the broadcast_view_propriety flag from a record in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetBroadcastViewPropriety","GetBroadcastViewPropriety method [Microsoft TV Technologies]","GetBroadcastViewPropriety method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetBroadcastViewPropriety method","IISDB_BIT.GetBroadcastViewPropriety","IISDB_BIT::GetBroadcastViewPropriety","dvbsiparser/IISDB_BIT::GetBroadcastViewPropriety","mstv.iisdb_bit_getbroadcastviewpropriety"]
old-location: mstv\iisdb_bit_getbroadcastviewpropriety.htm
tech.root: mstv
ms.assetid: b0b38631-9b0c-4ebe-9cf5-6e5847261136
ms.date: 12/05/2018
ms.keywords: GetBroadcastViewPropriety, GetBroadcastViewPropriety method [Microsoft TV Technologies], GetBroadcastViewPropriety method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetBroadcastViewPropriety method, IISDB_BIT.GetBroadcastViewPropriety, IISDB_BIT::GetBroadcastViewPropriety, dvbsiparser/IISDB_BIT::GetBroadcastViewPropriety, mstv.iisdb_bit_getbroadcastviewpropriety
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
 - IISDB_BIT::GetBroadcastViewPropriety
 - dvbsiparser/IISDB_BIT::GetBroadcastViewPropriety
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
 - IISDB_BIT.GetBroadcastViewPropriety
---

# IISDB_BIT::GetBroadcastViewPropriety


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns the broadcast_view_propriety flag from a record in
  an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT). The broadcast_view_propriety flag indicates whether the content associated with the broadcaster unit is appropriate for the age-based category of user.

## -parameters

### -param pbVal [out]

Receives the broadcast_view_propriety flag.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>