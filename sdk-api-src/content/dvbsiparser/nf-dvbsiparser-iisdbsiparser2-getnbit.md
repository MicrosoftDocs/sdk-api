---
UID: NF:dvbsiparser.IIsdbSiParser2.GetNBIT
title: IIsdbSiParser2::GetNBIT (dvbsiparser.h)
description: Gets the network board information table (NBIT) from an Integrated Services Digital Broadcast (ISDB) transport stream. The NBIT describes the programs included in a multiplexed transport stream.
helpviewer_keywords: ["GetNBIT","GetNBIT method [Microsoft TV Technologies]","GetNBIT method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetNBIT method","IIsdbSiParser2.GetNBIT","IIsdbSiParser2::GetNBIT","dvbsiparser/IIsdbSiParser2::GetNBIT","mstv.iisdbsiparser2_getnbit"]
old-location: mstv\iisdbsiparser2_getnbit.htm
tech.root: mstv
ms.assetid: 90c47d88-b364-4b42-b51b-dfa3c9eed4b0
ms.date: 12/05/2018
ms.keywords: GetNBIT, GetNBIT method [Microsoft TV Technologies], GetNBIT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetNBIT method, IIsdbSiParser2.GetNBIT, IIsdbSiParser2::GetNBIT, dvbsiparser/IIsdbSiParser2::GetNBIT, mstv.iisdbsiparser2_getnbit
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IIsdbSiParser2::GetNBIT
 - dvbsiparser/IIsdbSiParser2::GetNBIT
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
 - IIsdbSiParser2.GetNBIT
---

# IIsdbSiParser2::GetNBIT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the network board information table (NBIT) from an Integrated Services Digital Broadcast (ISDB) transport stream.
  The NBIT describes the programs included in a multiplexed transport stream.

## -parameters

### -param tableId [in]

Table identifier for the type of table to retrieve. For an NBIT, this value is 0xC5 if the table contains the network board information body, or 0xC6 if the table contains reference information for retrieving the network board information.

### -param pwOriginalNetworkId

Pointer to the original_network_id field for the NBIT. This field contains an identifier for the broadcaster that originates the
  MPEG-2 transport stream

### -param ppNBIT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>