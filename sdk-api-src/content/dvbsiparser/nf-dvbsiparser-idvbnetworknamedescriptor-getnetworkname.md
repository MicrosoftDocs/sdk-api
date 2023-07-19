---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetNetworkName
title: IDvbNetworkNameDescriptor::GetNetworkName (dvbsiparser.h)
description: Gets the network name, in ASCII string format, from a Digital Video Broadcast (DVB) network name descriptor.
helpviewer_keywords: ["GetNetworkName","GetNetworkName method [Microsoft TV Technologies]","GetNetworkName method [Microsoft TV Technologies]","IDvbNetworkNameDescriptor interface","IDvbNetworkNameDescriptor interface [Microsoft TV Technologies]","GetNetworkName method","IDvbNetworkNameDescriptor.GetNetworkName","IDvbNetworkNameDescriptor::GetNetworkName","dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkName","mstv.idvbnetworknamedescriptor_getnetworkname"]
old-location: mstv\idvbnetworknamedescriptor_getnetworkname.htm
tech.root: mstv
ms.assetid: 261a6c65-65a5-43ed-aaed-12968b996c5a
ms.date: 12/05/2018
ms.keywords: GetNetworkName, GetNetworkName method [Microsoft TV Technologies], GetNetworkName method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetNetworkName method, IDvbNetworkNameDescriptor.GetNetworkName, IDvbNetworkNameDescriptor::GetNetworkName, dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkName, mstv.idvbnetworknamedescriptor_getnetworkname
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
 - IDvbNetworkNameDescriptor::GetNetworkName
 - dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkName
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
 - IDvbNetworkNameDescriptor.GetNetworkName
---

# IDvbNetworkNameDescriptor::GetNetworkName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the network name, in ASCII string format, from a Digital Video Broadcast (DVB) network name  descriptor.

## -parameters

### -param pszName

Pointer to a buffer that receives the network name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbnetworknamedescriptor">IDvbNetworkNameDescriptor</a>