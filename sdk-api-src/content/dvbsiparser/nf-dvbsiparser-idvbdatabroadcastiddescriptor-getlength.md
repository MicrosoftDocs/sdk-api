---
UID: NF:dvbsiparser.IDvbDataBroadcastIDDescriptor.GetLength
title: IDvbDataBroadcastIDDescriptor::GetLength (dvbsiparser.h)
description: Gets the length (in bytes) of a Digital Video Broadcast (DVB) data broadcast ID descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbDataBroadcastIDDescriptor interface","IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbDataBroadcastIDDescriptor.GetLength","IDvbDataBroadcastIDDescriptor::GetLength","dvbsiparser/IDvbDataBroadcastIDDescriptor::GetLength","mstv.idvbdatabroadcastiddescriptor_getlength"]
old-location: mstv\idvbdatabroadcastiddescriptor_getlength.htm
tech.root: mstv
ms.assetid: f9727783-a876-40b4-b4fa-e839ef0f6502
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbDataBroadcastIDDescriptor interface, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbDataBroadcastIDDescriptor.GetLength, IDvbDataBroadcastIDDescriptor::GetLength, dvbsiparser/IDvbDataBroadcastIDDescriptor::GetLength, mstv.idvbdatabroadcastiddescriptor_getlength
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
 - IDvbDataBroadcastIDDescriptor::GetLength
 - dvbsiparser/IDvbDataBroadcastIDDescriptor::GetLength
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
 - IDvbDataBroadcastIDDescriptor.GetLength
---

# IDvbDataBroadcastIDDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length (in bytes) of 
  a Digital Video Broadcast (DVB) data broadcast ID descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastiddescriptor">IDvbDataBroadcastIDDescriptor</a>