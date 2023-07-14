---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetServiceId
title: IDvbLinkageDescriptor::GetServiceId (dvbsiparser.h)
description: Gets the identifier that identifies an information service in a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["GetServiceId","GetServiceId method [Microsoft TV Technologies]","GetServiceId method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetServiceId method","IDvbLinkageDescriptor.GetServiceId","IDvbLinkageDescriptor::GetServiceId","dvbsiparser/IDvbLinkageDescriptor::GetServiceId","mstv.idvblinkagedescriptor_getserviceid"]
old-location: mstv\idvblinkagedescriptor_getserviceid.htm
tech.root: mstv
ms.assetid: 977c284d-b995-4879-b90a-2bc42b60d1a3
ms.date: 12/05/2018
ms.keywords: GetServiceId, GetServiceId method [Microsoft TV Technologies], GetServiceId method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetServiceId method, IDvbLinkageDescriptor.GetServiceId, IDvbLinkageDescriptor::GetServiceId, dvbsiparser/IDvbLinkageDescriptor::GetServiceId, mstv.idvblinkagedescriptor_getserviceid
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
 - IDvbLinkageDescriptor::GetServiceId
 - dvbsiparser/IDvbLinkageDescriptor::GetServiceId
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
 - IDvbLinkageDescriptor.GetServiceId
---

# IDvbLinkageDescriptor::GetServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the identifier that identifies an information service in a Digital Video Broadcast (DVB) linkage descriptor.

## -parameters

### -param pwVal [out]

Receives the service identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>