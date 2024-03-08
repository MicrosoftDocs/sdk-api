---
UID: NF:dvbsiparser.IDvbDataBroadcastIDDescriptor.GetDataBroadcastID
title: IDvbDataBroadcastIDDescriptor::GetDataBroadcastID (dvbsiparser.h)
description: Gets the identifier that identifies the network broadcast from a Digital Video Broadcast (DVB) data broadcast descriptor.
helpviewer_keywords: ["GetDataBroadcastID","GetDataBroadcastID method [Microsoft TV Technologies]","GetDataBroadcastID method [Microsoft TV Technologies]","IDvbDataBroadcastIDDescriptor interface","IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies]","GetDataBroadcastID method","IDvbDataBroadcastIDDescriptor.GetDataBroadcastID","IDvbDataBroadcastIDDescriptor::GetDataBroadcastID","dvbsiparser/IDvbDataBroadcastIDDescriptor::GetDataBroadcastID","mstv.idvbdatabroadcastiddescriptor_getdatabroadcastid"]
old-location: mstv\idvbdatabroadcastiddescriptor_getdatabroadcastid.htm
tech.root: mstv
ms.assetid: 2addfb2b-80ab-47a7-81dd-f660e5fe1138
ms.date: 12/05/2018
ms.keywords: GetDataBroadcastID, GetDataBroadcastID method [Microsoft TV Technologies], GetDataBroadcastID method [Microsoft TV Technologies],IDvbDataBroadcastIDDescriptor interface, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],GetDataBroadcastID method, IDvbDataBroadcastIDDescriptor.GetDataBroadcastID, IDvbDataBroadcastIDDescriptor::GetDataBroadcastID, dvbsiparser/IDvbDataBroadcastIDDescriptor::GetDataBroadcastID, mstv.idvbdatabroadcastiddescriptor_getdatabroadcastid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbDataBroadcastIDDescriptor::GetDataBroadcastID
 - dvbsiparser/IDvbDataBroadcastIDDescriptor::GetDataBroadcastID
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
 - IDvbDataBroadcastIDDescriptor.GetDataBroadcastID
---

# IDvbDataBroadcastIDDescriptor::GetDataBroadcastID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the identifier that identifies the network broadcast from a Digital Video
Broadcast (DVB) data broadcast descriptor.

## -parameters

### -param pwVal [out]

Receives the broadcaster ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastiddescriptor">IDvbDataBroadcastIDDescriptor</a>