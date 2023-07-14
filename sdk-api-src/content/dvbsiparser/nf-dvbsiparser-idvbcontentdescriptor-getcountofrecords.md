---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetCountOfRecords
title: IDvbContentDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of content elements within a Digital Video Broadcast (DVB) content descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbContentDescriptor interface","IDvbContentDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbContentDescriptor.GetCountOfRecords","IDvbContentDescriptor::GetCountOfRecords","dvbsiparser/IDvbContentDescriptor::GetCountOfRecords","mstv.idvbcontentdescriptor_getcountofrecords"]
old-location: mstv\idvbcontentdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbContentDescriptor.GetCountOfRecords, IDvbContentDescriptor::GetCountOfRecords, dvbsiparser/IDvbContentDescriptor::GetCountOfRecords, mstv.idvbcontentdescriptor_getcountofrecords
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
 - IDvbContentDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbContentDescriptor::GetCountOfRecords
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
 - IDvbContentDescriptor.GetCountOfRecords
---

# IDvbContentDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of content elements within a Digital Video Broadcast (DVB)  content descriptor.

## -parameters

### -param pbVal [out]

Receives the number of content elements.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentdescriptor">IDvbContentDescriptor</a>