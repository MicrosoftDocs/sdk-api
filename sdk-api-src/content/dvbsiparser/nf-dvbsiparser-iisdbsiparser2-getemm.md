---
UID: NF:dvbsiparser.IIsdbSiParser2.GetEMM
title: IIsdbSiParser2::GetEMM (dvbsiparser.h)
description: Gets the entitlement management message (EMM) table from an Integrated Services Digital Broadcast (ISDB) transport stream.
helpviewer_keywords: ["GetEMM","GetEMM method [Microsoft TV Technologies]","GetEMM method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetEMM method","IIsdbSiParser2.GetEMM","IIsdbSiParser2::GetEMM","dvbsiparser/IIsdbSiParser2::GetEMM","mstv.iisdbsiparser2_getemm"]
old-location: mstv\iisdbsiparser2_getemm.htm
tech.root: mstv
ms.assetid: 9dc2aaa9-50f0-4c72-a252-3757a1aa13b7
ms.date: 12/05/2018
ms.keywords: GetEMM, GetEMM method [Microsoft TV Technologies], GetEMM method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetEMM method, IIsdbSiParser2.GetEMM, IIsdbSiParser2::GetEMM, dvbsiparser/IIsdbSiParser2::GetEMM, mstv.iisdbsiparser2_getemm
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
 - IIsdbSiParser2::GetEMM
 - dvbsiparser/IIsdbSiParser2::GetEMM
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
 - IIsdbSiParser2.GetEMM
---

# IIsdbSiParser2::GetEMM


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 
  Gets the entitlement management message (EMM) table from an Integrated Services Digital Broadcast (ISDB) transport stream. An EMM contains conditional access data, such as contract
  information for subscribers, keys to decrypt common information, and the
  authorization levels or services of specific decoders.

## -parameters

### -param pid [in]

Specifies the packet identifier (PID) of the transport stream packet that transmits the EMM.

### -param wTableIdExt [in]

Value of the table_id field for the EMM. This field value identifies a subtable in the EMM.

### -param ppEMM [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>