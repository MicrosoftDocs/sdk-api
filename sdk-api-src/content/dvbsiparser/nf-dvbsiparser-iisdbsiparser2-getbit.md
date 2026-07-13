---
UID: NF:dvbsiparser.IIsdbSiParser2.GetBIT
title: IIsdbSiParser2::GetBIT (dvbsiparser.h)
description: Gets the broadcaster information table (BIT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A BIT contains a broadcaster unit and the service information transmission parameter for each broadcaster unit.
helpviewer_keywords: ["GetBIT","GetBIT method [Microsoft TV Technologies]","GetBIT method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetBIT method","IIsdbSiParser2.GetBIT","IIsdbSiParser2::GetBIT","dvbsiparser/IIsdbSiParser2::GetBIT","mstv.iisdbsiparser2_getbit"]
old-location: mstv\iisdbsiparser2_getbit.htm
tech.root: mstv
ms.assetid: 25993059-a1a9-486f-97b3-fd240c8931dc
ms.date: 12/05/2018
ms.keywords: GetBIT, GetBIT method [Microsoft TV Technologies], GetBIT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetBIT method, IIsdbSiParser2.GetBIT, IIsdbSiParser2::GetBIT, dvbsiparser/IIsdbSiParser2::GetBIT, mstv.iisdbsiparser2_getbit
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
 - IIsdbSiParser2::GetBIT
 - dvbsiparser/IIsdbSiParser2::GetBIT
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
 - IIsdbSiParser2.GetBIT
---

# IIsdbSiParser2::GetBIT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the broadcaster information table (BIT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A BIT contains a broadcaster unit and the service information transmission parameter
  for each broadcaster unit.

## -parameters

### -param tableId [in]

Table identifier for the type of table to retrieve. For a BIT, this value is 0xC4.

### -param pwOriginalNetworkId

Pointer to the original_network_id field for the BIT. This field contains an identifier for the broadcaster that originates the
  MPEG-2 transport stream

### -param ppBIT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>