---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetLength
title: IDvbMultilingualServiceNameDescriptor::GetLength (dvbsiparser.h)
description: Gets the descriptor_length field value from a from a Digital Video Broadcast (DVB) multilingual service name descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbMultilingualServiceNameDescriptor interface","IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbMultilingualServiceNameDescriptor.GetLength","IDvbMultilingualServiceNameDescriptor::GetLength","dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetLength","mstv.idvbmultilingualservicenamedescriptor_getlength"]
old-location: mstv\idvbmultilingualservicenamedescriptor_getlength.htm
tech.root: mstv
ms.assetid: 851d3d7b-0891-41a7-899e-61aac641ab3c
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbMultilingualServiceNameDescriptor interface, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbMultilingualServiceNameDescriptor.GetLength, IDvbMultilingualServiceNameDescriptor::GetLength, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetLength, mstv.idvbmultilingualservicenamedescriptor_getlength
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
 - IDvbMultilingualServiceNameDescriptor::GetLength
 - dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetLength
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
 - IDvbMultilingualServiceNameDescriptor.GetLength
---

# IDvbMultilingualServiceNameDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the descriptor_length field value from a from a Digital Video Broadcast (DVB) multilingual service name descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor_length field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbmultilingualservicenamedescriptor">IDvbMultilingualServiceNameDescriptor</a>