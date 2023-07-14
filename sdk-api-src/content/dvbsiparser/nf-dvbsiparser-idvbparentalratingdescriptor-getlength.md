---
UID: NF:dvbsiparser.IDvbParentalRatingDescriptor.GetLength
title: IDvbParentalRatingDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) parental rating descriptor, in bytes,.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbParentalRatingDescriptor interface","IDvbParentalRatingDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbParentalRatingDescriptor.GetLength","IDvbParentalRatingDescriptor::GetLength","dvbsiparser/IDvbParentalRatingDescriptor::GetLength","mstv.idvbparentalratingdescriptor_getlength"]
old-location: mstv\idvbparentalratingdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 019c6998-74b3-4966-ad5d-b8da2bbacca5
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbParentalRatingDescriptor interface, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbParentalRatingDescriptor.GetLength, IDvbParentalRatingDescriptor::GetLength, dvbsiparser/IDvbParentalRatingDescriptor::GetLength, mstv.idvbparentalratingdescriptor_getlength
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
 - IDvbParentalRatingDescriptor::GetLength
 - dvbsiparser/IDvbParentalRatingDescriptor::GetLength
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
 - IDvbParentalRatingDescriptor.GetLength
---

# IDvbParentalRatingDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the body length of a Digital Video Broadcast (DVB) parental rating descriptor, in bytes,.

## -parameters

### -param pbVal [out]

Receives the descriptor length, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbparentalratingdescriptor">IDvbParentalRatingDescriptor</a>