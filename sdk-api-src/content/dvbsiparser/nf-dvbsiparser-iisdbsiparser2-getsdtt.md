---
UID: NF:dvbsiparser.IIsdbSiParser2.GetSDTT
title: IIsdbSiParser2::GetSDTT (dvbsiparser.h)
description: Gets the software download trigger table (SDTT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDTT contains download information such as the service identifier, schedule, and receiver types for revision.
helpviewer_keywords: ["GetSDTT","GetSDTT method [Microsoft TV Technologies]","GetSDTT method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetSDTT method","IIsdbSiParser2.GetSDTT","IIsdbSiParser2::GetSDTT","dvbsiparser/IIsdbSiParser2::GetSDTT","mstv.iisdbsiparser2_getsdtt"]
old-location: mstv\iisdbsiparser2_getsdtt.htm
tech.root: mstv
ms.assetid: fd361526-eb0c-4edd-b346-3bded48fdc06
ms.date: 12/05/2018
ms.keywords: GetSDTT, GetSDTT method [Microsoft TV Technologies], GetSDTT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetSDTT method, IIsdbSiParser2.GetSDTT, IIsdbSiParser2::GetSDTT, dvbsiparser/IIsdbSiParser2::GetSDTT, mstv.iisdbsiparser2_getsdtt
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
 - IIsdbSiParser2::GetSDTT
 - dvbsiparser/IIsdbSiParser2::GetSDTT
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
 - IIsdbSiParser2.GetSDTT
---

# IIsdbSiParser2::GetSDTT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

  Gets the software download
  trigger table
  (SDTT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDTT contains download information such as the service identifier, schedule, and
  receiver types for revision.

## -parameters

### -param tableId [in]

Table identifier for the type of table to retrieve. For an SDTT, this value is 0xC34.

### -param pwTableIdExt

Value of the table_id_extension field for the SDTT. This field value identifies a specific instance of the SDTT.

### -param ppSDTT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>