---
UID: NF:dvbsiparser.IDvbPrivateDataSpecifierDescriptor.GetLength
title: IDvbPrivateDataSpecifierDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) private data descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbPrivateDataSpecifierDescriptor interface","IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbPrivateDataSpecifierDescriptor.GetLength","IDvbPrivateDataSpecifierDescriptor::GetLength","dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetLength","mstv.idvbprivatedataspecifierdescriptor_getlength"]
old-location: mstv\idvbprivatedataspecifierdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 9a3b550c-3082-4ac8-9568-6ccdec26d193
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbPrivateDataSpecifierDescriptor interface, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbPrivateDataSpecifierDescriptor.GetLength, IDvbPrivateDataSpecifierDescriptor::GetLength, dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetLength, mstv.idvbprivatedataspecifierdescriptor_getlength
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
 - IDvbPrivateDataSpecifierDescriptor::GetLength
 - dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetLength
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
 - IDvbPrivateDataSpecifierDescriptor.GetLength
---

# IDvbPrivateDataSpecifierDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body  length of a Digital Video Broadcast (DVB) private data descriptor.

## -parameters

### -param pbVal [out]

Receives the private data descriptor length, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbprivatedataspecifierdescriptor">IDvbPrivateDataSpecifierDescriptor</a>