---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetCountOfRecords
title: IDvbSubtitlingDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of subtitling records in a Digital Video Broadcast (DVB) subtitling descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbSubtitlingDescriptor interface","IDvbSubtitlingDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbSubtitlingDescriptor.GetCountOfRecords","IDvbSubtitlingDescriptor::GetCountOfRecords","dvbsiparser/IDvbSubtitlingDescriptor::GetCountOfRecords","mstv.idvbsubtitlingdescriptor_getcountofrecords"]
old-location: mstv\idvbsubtitlingdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 8cc25b63-de43-4f8d-af19-c3bb8c389a55
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbSubtitlingDescriptor.GetCountOfRecords, IDvbSubtitlingDescriptor::GetCountOfRecords, dvbsiparser/IDvbSubtitlingDescriptor::GetCountOfRecords, mstv.idvbsubtitlingdescriptor_getcountofrecords
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
 - IDvbSubtitlingDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbSubtitlingDescriptor::GetCountOfRecords
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
 - IDvbSubtitlingDescriptor.GetCountOfRecords
---

# IDvbSubtitlingDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of subtitling records in a Digital Video Broadcast (DVB)  subtitling descriptor.

## -parameters

### -param pbVal [out]

Returns the number of subtitling records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>