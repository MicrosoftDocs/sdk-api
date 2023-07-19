---
UID: NF:dvbsiparser.IDvbParentalRatingDescriptor.GetCountOfRecords
title: IDvbParentalRatingDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in a Digital Video Broadcast (DVB) parental rating descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbParentalRatingDescriptor interface","IDvbParentalRatingDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbParentalRatingDescriptor.GetCountOfRecords","IDvbParentalRatingDescriptor::GetCountOfRecords","dvbsiparser/IDvbParentalRatingDescriptor::GetCountOfRecords","mstv.idvbparentalratingdescriptor_getcountofrecords"]
old-location: mstv\idvbparentalratingdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 72dcfb91-4137-4149-b30d-2551cb209688
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbParentalRatingDescriptor interface, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbParentalRatingDescriptor.GetCountOfRecords, IDvbParentalRatingDescriptor::GetCountOfRecords, dvbsiparser/IDvbParentalRatingDescriptor::GetCountOfRecords, mstv.idvbparentalratingdescriptor_getcountofrecords
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
 - IDvbParentalRatingDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbParentalRatingDescriptor::GetCountOfRecords
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
 - IDvbParentalRatingDescriptor.GetCountOfRecords
---

# IDvbParentalRatingDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in  a Digital Video Broadcast (DVB) parental rating descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbparentalratingdescriptor">IDvbParentalRatingDescriptor</a>