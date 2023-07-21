---
UID: NF:dvbsiparser.IDvbPrivateDataSpecifierDescriptor.GetPrivateDataSpecifier
title: IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier (dvbsiparser.h)
description: Gets the data from a Digital Video Broadcast (DVB) private data descriptor.
helpviewer_keywords: ["GetPrivateDataSpecifier","GetPrivateDataSpecifier method [Microsoft TV Technologies]","GetPrivateDataSpecifier method [Microsoft TV Technologies]","IDvbPrivateDataSpecifierDescriptor interface","IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies]","GetPrivateDataSpecifier method","IDvbPrivateDataSpecifierDescriptor.GetPrivateDataSpecifier","IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier","dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier","mstv.idvbprivatedataspecifierdescriptor_getprivatedataspecifier"]
old-location: mstv\idvbprivatedataspecifierdescriptor_getprivatedataspecifier.htm
tech.root: mstv
ms.assetid: bb5b7d8a-6699-49b4-8935-8bfd07d85290
ms.date: 12/05/2018
ms.keywords: GetPrivateDataSpecifier, GetPrivateDataSpecifier method [Microsoft TV Technologies], GetPrivateDataSpecifier method [Microsoft TV Technologies],IDvbPrivateDataSpecifierDescriptor interface, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies],GetPrivateDataSpecifier method, IDvbPrivateDataSpecifierDescriptor.GetPrivateDataSpecifier, IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier, dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier, mstv.idvbprivatedataspecifierdescriptor_getprivatedataspecifier
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
 - IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier
 - dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier
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
 - IDvbPrivateDataSpecifierDescriptor.GetPrivateDataSpecifier
---

# IDvbPrivateDataSpecifierDescriptor::GetPrivateDataSpecifier


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the data from  a Digital Video Broadcast (DVB) private data descriptor.

## -parameters

### -param pdwVal [out]

Receives the private descriptor specifier data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbprivatedataspecifierdescriptor">IDvbPrivateDataSpecifierDescriptor</a>