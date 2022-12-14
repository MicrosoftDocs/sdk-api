---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetLength
title: IDvbNetworkNameDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) network name descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbNetworkNameDescriptor interface","IDvbNetworkNameDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbNetworkNameDescriptor.GetLength","IDvbNetworkNameDescriptor::GetLength","dvbsiparser/IDvbNetworkNameDescriptor::GetLength","mstv.idvbnetworknamedescriptor_getlength"]
old-location: mstv\idvbnetworknamedescriptor_getlength.htm
tech.root: mstv
ms.assetid: 22841428-c223-4385-97c3-bd1819468866
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbNetworkNameDescriptor.GetLength, IDvbNetworkNameDescriptor::GetLength, dvbsiparser/IDvbNetworkNameDescriptor::GetLength, mstv.idvbnetworknamedescriptor_getlength
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
 - IDvbNetworkNameDescriptor::GetLength
 - dvbsiparser/IDvbNetworkNameDescriptor::GetLength
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
 - IDvbNetworkNameDescriptor.GetLength
---

# IDvbNetworkNameDescriptor::GetLength


## -description

Gets the body length of a Digital Video Broadcast (DVB) network name descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor length, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbnetworknamedescriptor">IDvbNetworkNameDescriptor</a>