---
UID: NF:dvbsiparser.IDvbContentIdentifierDescriptor.GetCountOfRecords
title: IDvbContentIdentifierDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of service records in a Digital Video Broadcast (DVB) content identifier descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbContentIdentifierDescriptor interface","IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbContentIdentifierDescriptor.GetCountOfRecords","IDvbContentIdentifierDescriptor::GetCountOfRecords","dvbsiparser/IDvbContentIdentifierDescriptor::GetCountOfRecords","mstv.idvbcontentidentifierdescriptor_getcountofrecords"]
old-location: mstv\idvbcontentidentifierdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: cd96a052-52e6-4de7-aa44-66c2caa4d5f5
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbContentIdentifierDescriptor interface, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbContentIdentifierDescriptor.GetCountOfRecords, IDvbContentIdentifierDescriptor::GetCountOfRecords, dvbsiparser/IDvbContentIdentifierDescriptor::GetCountOfRecords, mstv.idvbcontentidentifierdescriptor_getcountofrecords
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
 - IDvbContentIdentifierDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbContentIdentifierDescriptor::GetCountOfRecords
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
 - IDvbContentIdentifierDescriptor.GetCountOfRecords
---

# IDvbContentIdentifierDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of service records in a Digital Video Broadcast (DVB)  content identifier descriptor.

## -parameters

### -param pbVal [out]

Receives the number of service records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentidentifierdescriptor">IDvbContentIdentifierDescriptor</a>