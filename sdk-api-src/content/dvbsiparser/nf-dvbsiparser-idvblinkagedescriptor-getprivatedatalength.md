---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetPrivateDataLength
title: IDvbLinkageDescriptor::GetPrivateDataLength (dvbsiparser.h)
description: Gets the length of the private data field from a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["GetPrivateDataLength","GetPrivateDataLength method [Microsoft TV Technologies]","GetPrivateDataLength method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetPrivateDataLength method","IDvbLinkageDescriptor.GetPrivateDataLength","IDvbLinkageDescriptor::GetPrivateDataLength","dvbsiparser/IDvbLinkageDescriptor::GetPrivateDataLength","mstv.idvblinkagedescriptor_getprivatedatalength"]
old-location: mstv\idvblinkagedescriptor_getprivatedatalength.htm
tech.root: mstv
ms.assetid: 6c37a877-5a0e-49ed-bf75-bb8ad73fa783
ms.date: 12/05/2018
ms.keywords: GetPrivateDataLength, GetPrivateDataLength method [Microsoft TV Technologies], GetPrivateDataLength method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetPrivateDataLength method, IDvbLinkageDescriptor.GetPrivateDataLength, IDvbLinkageDescriptor::GetPrivateDataLength, dvbsiparser/IDvbLinkageDescriptor::GetPrivateDataLength, mstv.idvblinkagedescriptor_getprivatedatalength
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
 - IDvbLinkageDescriptor::GetPrivateDataLength
 - dvbsiparser/IDvbLinkageDescriptor::GetPrivateDataLength
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
 - IDvbLinkageDescriptor.GetPrivateDataLength
---

# IDvbLinkageDescriptor::GetPrivateDataLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of the private data field from a Digital Video Broadcast (DVB) linkage descriptor.

## -parameters

### -param pbVal [out]

Receives the length of the private data field, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>