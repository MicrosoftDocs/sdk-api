---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetCountOfRecords
title: IDvbExtendedEventDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of item records in a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbExtendedEventDescriptor.GetCountOfRecords","IDvbExtendedEventDescriptor::GetCountOfRecords","dvbsiparser/IDvbExtendedEventDescriptor::GetCountOfRecords","mstv.idvbextendedeventdescriptor_getcountofrecords"]
old-location: mstv\idvbextendedeventdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: db065f1a-8354-4207-b7f7-d67adf094c70
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbExtendedEventDescriptor.GetCountOfRecords, IDvbExtendedEventDescriptor::GetCountOfRecords, dvbsiparser/IDvbExtendedEventDescriptor::GetCountOfRecords, mstv.idvbextendedeventdescriptor_getcountofrecords
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
 - IDvbExtendedEventDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbExtendedEventDescriptor::GetCountOfRecords
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
 - IDvbExtendedEventDescriptor.GetCountOfRecords
---

# IDvbExtendedEventDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of item records in a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param pbVal [out]

Receives the number of item records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>