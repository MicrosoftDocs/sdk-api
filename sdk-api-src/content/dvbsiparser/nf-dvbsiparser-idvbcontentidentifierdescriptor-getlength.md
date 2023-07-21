---
UID: NF:dvbsiparser.IDvbContentIdentifierDescriptor.GetLength
title: IDvbContentIdentifierDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) content identifier descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbContentIdentifierDescriptor interface","IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbContentIdentifierDescriptor.GetLength","IDvbContentIdentifierDescriptor::GetLength","dvbsiparser/IDvbContentIdentifierDescriptor::GetLength","mstv.idvbcontentidentifierdescriptor_getlength"]
old-location: mstv\idvbcontentidentifierdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 0138416a-70d6-4a64-957b-8b0eb031b589
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbContentIdentifierDescriptor interface, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbContentIdentifierDescriptor.GetLength, IDvbContentIdentifierDescriptor::GetLength, dvbsiparser/IDvbContentIdentifierDescriptor::GetLength, mstv.idvbcontentidentifierdescriptor_getlength
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
 - IDvbContentIdentifierDescriptor::GetLength
 - dvbsiparser/IDvbContentIdentifierDescriptor::GetLength
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
 - IDvbContentIdentifierDescriptor.GetLength
---

# IDvbContentIdentifierDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of a Digital Video Broadcast (DVB)  content identifier descriptor.

## -parameters

### -param pbVal [out]

Gets the descriptor body length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentidentifierdescriptor">IDvbContentIdentifierDescriptor</a>