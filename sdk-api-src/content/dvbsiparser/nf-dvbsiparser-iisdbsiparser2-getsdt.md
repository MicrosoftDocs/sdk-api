---
UID: NF:dvbsiparser.IIsdbSiParser2.GetSDT
title: IIsdbSiParser2::GetSDT (dvbsiparser.h)
description: Gets a service description table (SDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDT lists the names and other parameters of the services in an MPEG-2 transport stream.
helpviewer_keywords: ["GetSDT","GetSDT method [Microsoft TV Technologies]","GetSDT method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetSDT method","IIsdbSiParser2.GetSDT","IIsdbSiParser2::GetSDT","dvbsiparser/IIsdbSiParser2::GetSDT","mstv.iisdbsiparser2_getsdt"]
old-location: mstv\iisdbsiparser2_getsdt.htm
tech.root: mstv
ms.assetid: d15d1b6a-5b53-4962-89a3-9bd06e00d366
ms.date: 12/05/2018
ms.keywords: GetSDT, GetSDT method [Microsoft TV Technologies], GetSDT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetSDT method, IIsdbSiParser2.GetSDT, IIsdbSiParser2::GetSDT, dvbsiparser/IIsdbSiParser2::GetSDT, mstv.iisdbsiparser2_getsdt
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
 - IIsdbSiParser2::GetSDT
 - dvbsiparser/IIsdbSiParser2::GetSDT
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
 - IIsdbSiParser2.GetSDT
---

# IIsdbSiParser2::GetSDT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a
  service description table (SDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDT
  lists the names and other parameters of the services in an MPEG-2 transport stream.

## -parameters

### -param tableId [in]

Table identifier for the type of table to retrieve. For an SDT, this value is 0x42 for an actual transport stream, or 0x46 for another stream.

### -param pwTransportStreamId

Pointer to the transport_stream_id field. This field value uniquely identifies the transport stream that contains the SDT.

### -param ppSDT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdt">IISDB_SDT</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdt">IISDB_SDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>