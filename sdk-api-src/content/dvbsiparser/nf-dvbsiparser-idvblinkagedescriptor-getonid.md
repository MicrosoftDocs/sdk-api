---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetONId
title: IDvbLinkageDescriptor::GetONId (dvbsiparser.h)
description: Gets the network identifier of the broadcast system that originated an information service from a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["GetONId","GetONId method [Microsoft TV Technologies]","GetONId method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetONId method","IDvbLinkageDescriptor.GetONId","IDvbLinkageDescriptor::GetONId","dvbsiparser/IDvbLinkageDescriptor::GetONId","mstv.idvblinkagedescriptor_getonid"]
old-location: mstv\idvblinkagedescriptor_getonid.htm
tech.root: mstv
ms.assetid: e7c27f45-032a-46d5-b5ae-8a4ef2ee2ebc
ms.date: 12/05/2018
ms.keywords: GetONId, GetONId method [Microsoft TV Technologies], GetONId method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetONId method, IDvbLinkageDescriptor.GetONId, IDvbLinkageDescriptor::GetONId, dvbsiparser/IDvbLinkageDescriptor::GetONId, mstv.idvblinkagedescriptor_getonid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbLinkageDescriptor::GetONId
 - dvbsiparser/IDvbLinkageDescriptor::GetONId
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
 - IDvbLinkageDescriptor.GetONId
---

# IDvbLinkageDescriptor::GetONId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the network identifier of the  broadcast system that originated an information service from a Digital Video Broadcast (DVB) linkage descriptor.

## -parameters

### -param pwVal [out]

Receives the network identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>