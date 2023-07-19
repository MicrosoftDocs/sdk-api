---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetLength
title: IDvbLinkageDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbLinkageDescriptor.GetLength","IDvbLinkageDescriptor::GetLength","dvbsiparser/IDvbLinkageDescriptor::GetLength","mstv.idvblinkagedescriptor_getlength"]
old-location: mstv\idvblinkagedescriptor_getlength.htm
tech.root: mstv
ms.assetid: b6a4e072-3abe-4305-811d-2bdb846ce028
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbLinkageDescriptor.GetLength, IDvbLinkageDescriptor::GetLength, dvbsiparser/IDvbLinkageDescriptor::GetLength, mstv.idvblinkagedescriptor_getlength
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
 - IDvbLinkageDescriptor::GetLength
 - dvbsiparser/IDvbLinkageDescriptor::GetLength
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
 - IDvbLinkageDescriptor.GetLength
---

# IDvbLinkageDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of a Digital Video Broadcast (DVB) linkage descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor length, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>