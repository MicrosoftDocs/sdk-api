---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordCompositionPageID
title: IDvbSubtitlingDescriptor::GetRecordCompositionPageID (dvbsiparser.h)
description: Gets the composition page identifier for a Digital Video Broadcast (DVB) subtitling descriptor.
helpviewer_keywords: ["GetRecordCompositionPageID","GetRecordCompositionPageID method [Microsoft TV Technologies]","GetRecordCompositionPageID method [Microsoft TV Technologies]","IDvbSubtitlingDescriptor interface","IDvbSubtitlingDescriptor interface [Microsoft TV Technologies]","GetRecordCompositionPageID method","IDvbSubtitlingDescriptor.GetRecordCompositionPageID","IDvbSubtitlingDescriptor::GetRecordCompositionPageID","dvbsiparser/IDvbSubtitlingDescriptor::GetRecordCompositionPageID","mstv.idvbsubtitlingdescriptor_getrecordcompositionpageid"]
old-location: mstv\idvbsubtitlingdescriptor_getrecordcompositionpageid.htm
tech.root: mstv
ms.assetid: 108f431a-e3c3-42d5-ad27-b7a54029051f
ms.date: 12/05/2018
ms.keywords: GetRecordCompositionPageID, GetRecordCompositionPageID method [Microsoft TV Technologies], GetRecordCompositionPageID method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordCompositionPageID method, IDvbSubtitlingDescriptor.GetRecordCompositionPageID, IDvbSubtitlingDescriptor::GetRecordCompositionPageID, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordCompositionPageID, mstv.idvbsubtitlingdescriptor_getrecordcompositionpageid
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
 - IDvbSubtitlingDescriptor::GetRecordCompositionPageID
 - dvbsiparser/IDvbSubtitlingDescriptor::GetRecordCompositionPageID
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
 - IDvbSubtitlingDescriptor.GetRecordCompositionPageID
---

# IDvbSubtitlingDescriptor::GetRecordCompositionPageID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the composition page identifier for a Digital Video Broadcast (DVB) subtitling descriptor. DVB subtitling segments that signal a
composition page identifier are decoded if the previous data in the subtitling descriptor matches the user's selection criteria.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>

### -param pwVal [out]

Receives the composition page identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The composition page identifier is signalled in at least the subtitling segments that define the data
structure of the subtitle screen: the page composition segment and region composition segments. It
may additionally be signalled in segments containing data on which the composition depends.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>