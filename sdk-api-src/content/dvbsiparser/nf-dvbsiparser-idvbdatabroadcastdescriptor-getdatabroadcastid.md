---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetDataBroadcastID
title: IDvbDataBroadcastDescriptor::GetDataBroadcastID (dvbsiparser.h)
description: Gets the identifier that identifies the network broadcast from a Digital Video Broadcast (DVB) data broadcast descriptor.
helpviewer_keywords: ["GetDataBroadcastID","GetDataBroadcastID method [Microsoft TV Technologies]","GetDataBroadcastID method [Microsoft TV Technologies]","IDvbDataBroadcastDescriptor interface","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","GetDataBroadcastID method","IDvbDataBroadcastDescriptor.GetDataBroadcastID","IDvbDataBroadcastDescriptor::GetDataBroadcastID","dvbsiparser/IDvbDataBroadcastDescriptor::GetDataBroadcastID","mstv.idvbdatabroadcastdescriptor_getdatabroadcastid"]
old-location: mstv\idvbdatabroadcastdescriptor_getdatabroadcastid.htm
tech.root: mstv
ms.assetid: 0124e197-85a0-47bf-afb6-100c344e9c9e
ms.date: 12/05/2018
ms.keywords: GetDataBroadcastID, GetDataBroadcastID method [Microsoft TV Technologies], GetDataBroadcastID method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetDataBroadcastID method, IDvbDataBroadcastDescriptor.GetDataBroadcastID, IDvbDataBroadcastDescriptor::GetDataBroadcastID, dvbsiparser/IDvbDataBroadcastDescriptor::GetDataBroadcastID, mstv.idvbdatabroadcastdescriptor_getdatabroadcastid
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
 - IDvbDataBroadcastDescriptor::GetDataBroadcastID
 - dvbsiparser/IDvbDataBroadcastDescriptor::GetDataBroadcastID
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
 - IDvbDataBroadcastDescriptor.GetDataBroadcastID
---

# IDvbDataBroadcastDescriptor::GetDataBroadcastID


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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastdescriptor">IDvbDataBroadcastDescriptor</a>