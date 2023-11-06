---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetTag
title: IDvbNetworkNameDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a Digital Video Broadcast (DVB) network name descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbNetworkNameDescriptor interface","IDvbNetworkNameDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbNetworkNameDescriptor.GetTag","IDvbNetworkNameDescriptor::GetTag","dvbsiparser/IDvbNetworkNameDescriptor::GetTag","mstv.idvbnetworknamedescriptor_gettag"]
old-location: mstv\idvbnetworknamedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 9bc0ffea-ef18-488e-adeb-a5fd19b343a6
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbNetworkNameDescriptor.GetTag, IDvbNetworkNameDescriptor::GetTag, dvbsiparser/IDvbNetworkNameDescriptor::GetTag, mstv.idvbnetworknamedescriptor_gettag
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
 - IDvbNetworkNameDescriptor::GetTag
 - dvbsiparser/IDvbNetworkNameDescriptor::GetTag
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
 - IDvbNetworkNameDescriptor.GetTag
---

# IDvbNetworkNameDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a Digital Video Broadcast (DVB) network name descriptor.

## -parameters

### -param pbVal [out]

Receives the identifier tag. For DVB network name descriptors, this value is "0x40".

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbnetworknamedescriptor">IDvbNetworkNameDescriptor</a>