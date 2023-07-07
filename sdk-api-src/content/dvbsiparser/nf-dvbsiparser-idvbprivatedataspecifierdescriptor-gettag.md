---
UID: NF:dvbsiparser.IDvbPrivateDataSpecifierDescriptor.GetTag
title: IDvbPrivateDataSpecifierDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a Digital Video Broadcast (DVB) private data descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbPrivateDataSpecifierDescriptor interface","IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbPrivateDataSpecifierDescriptor.GetTag","IDvbPrivateDataSpecifierDescriptor::GetTag","dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetTag","mstv.idvbprivatedataspecifierdescriptor_gettag"]
old-location: mstv\idvbprivatedataspecifierdescriptor_gettag.htm
tech.root: mstv
ms.assetid: bccca68c-d480-47d0-a0db-7a7d3f8376c2
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbPrivateDataSpecifierDescriptor interface, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbPrivateDataSpecifierDescriptor.GetTag, IDvbPrivateDataSpecifierDescriptor::GetTag, dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetTag, mstv.idvbprivatedataspecifierdescriptor_gettag
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
 - IDvbPrivateDataSpecifierDescriptor::GetTag
 - dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetTag
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
 - IDvbPrivateDataSpecifierDescriptor.GetTag
---

# IDvbPrivateDataSpecifierDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a Digital Video Broadcast (DVB) private data descriptor.

## -parameters

### -param pbVal [out]

Receives the private descriptor identifier tag. For private data descriptors, this value is 0x5F.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbprivatedataspecifierdescriptor">IDvbPrivateDataSpecifierDescriptor</a>