---
UID: NF:dvbsiparser.IIsdbSiParser2.GetLDT
title: IIsdbSiParser2::GetLDT (dvbsiparser.h)
description: Gets a linked description table (LDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An LDT contains data that is used to collect reference information from other tables.
helpviewer_keywords: ["GetLDT","GetLDT method [Microsoft TV Technologies]","GetLDT method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetLDT method","IIsdbSiParser2.GetLDT","IIsdbSiParser2::GetLDT","dvbsiparser/IIsdbSiParser2::GetLDT","mstv.iisdbsiparser2_getldt"]
old-location: mstv\iisdbsiparser2_getldt.htm
tech.root: mstv
ms.assetid: b4b91e95-cf0f-488b-9941-4d1d81dc7661
ms.date: 12/05/2018
ms.keywords: GetLDT, GetLDT method [Microsoft TV Technologies], GetLDT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetLDT method, IIsdbSiParser2.GetLDT, IIsdbSiParser2::GetLDT, dvbsiparser/IIsdbSiParser2::GetLDT, mstv.iisdbsiparser2_getldt
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
 - IIsdbSiParser2::GetLDT
 - dvbsiparser/IIsdbSiParser2::GetLDT
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
 - IIsdbSiParser2.GetLDT
---

# IIsdbSiParser2::GetLDT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a 
  linked description table (LDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An LDT contains data that is used to collect reference
  information from other tables.

## -parameters

### -param tableId [in]

Table identifier for the type of table to retrieve. For an LDT, this value is 0xC7.

### -param pwOriginalServiceId

Pointer to the original_service_id field for the LDT. This field contains an identifier for the service  for this transport stream.

### -param ppLDT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>