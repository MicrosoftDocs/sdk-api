---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordAncillaryPageID
title: IDvbSubtitlingDescriptor::GetRecordAncillaryPageID (dvbsiparser.h)
description: Gets the ancillary page identifier for a Digital Video Broadcast (DVB) subtitling descriptor.
helpviewer_keywords: ["GetRecordAncillaryPageID","GetRecordAncillaryPageID method [Microsoft TV Technologies]","GetRecordAncillaryPageID method [Microsoft TV Technologies]","IDvbSubtitlingDescriptor interface","IDvbSubtitlingDescriptor interface [Microsoft TV Technologies]","GetRecordAncillaryPageID method","IDvbSubtitlingDescriptor.GetRecordAncillaryPageID","IDvbSubtitlingDescriptor::GetRecordAncillaryPageID","dvbsiparser/IDvbSubtitlingDescriptor::GetRecordAncillaryPageID","mstv.idvbsubtitlingdescriptor_getrecordancillarypageid"]
old-location: mstv\idvbsubtitlingdescriptor_getrecordancillarypageid.htm
tech.root: mstv
ms.assetid: ab490087-063d-4e9f-8aa5-679804548d26
ms.date: 12/05/2018
ms.keywords: GetRecordAncillaryPageID, GetRecordAncillaryPageID method [Microsoft TV Technologies], GetRecordAncillaryPageID method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordAncillaryPageID method, IDvbSubtitlingDescriptor.GetRecordAncillaryPageID, IDvbSubtitlingDescriptor::GetRecordAncillaryPageID, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordAncillaryPageID, mstv.idvbsubtitlingdescriptor_getrecordancillarypageid
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
 - IDvbSubtitlingDescriptor::GetRecordAncillaryPageID
 - dvbsiparser/IDvbSubtitlingDescriptor::GetRecordAncillaryPageID
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
 - IDvbSubtitlingDescriptor.GetRecordAncillaryPageID
---

# IDvbSubtitlingDescriptor::GetRecordAncillaryPageID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the ancillary page identifier for a Digital Video Broadcast (DVB) subtitling descriptor.  The DVB subtitling segments signalling the ancillary page identifier are decoded if the previous data in the subtitling descriptor matches the user's selection criteria.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>

### -param pwVal [out]

Receives the ancillary page identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the subtitling descriptor has no ancillary page, the values in
the ancillary_page_id and composition_page_id fields of the descriptor are the same.

 The ancillary_page_id is never signalled in a composition segment. It may be signalled in color
lookup table (CLUT) definition segments, object segments, or any other type of segment.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>