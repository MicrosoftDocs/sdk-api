---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetRecordUserNibbles
title: IDvbContentDescriptor::GetRecordUserNibbles (dvbsiparser.h)
description: Gets the two 4-bit fields that make up a broadcaster-defined identifier for a content descriptor.
helpviewer_keywords: ["GetRecordUserNibbles","GetRecordUserNibbles method [Microsoft TV Technologies]","GetRecordUserNibbles method [Microsoft TV Technologies]","IDvbContentDescriptor interface","IDvbContentDescriptor interface [Microsoft TV Technologies]","GetRecordUserNibbles method","IDvbContentDescriptor.GetRecordUserNibbles","IDvbContentDescriptor::GetRecordUserNibbles","dvbsiparser/IDvbContentDescriptor::GetRecordUserNibbles","mstv.idvbcontentdescriptor_getrecordusernibbles"]
old-location: mstv\idvbcontentdescriptor_getrecordusernibbles.htm
tech.root: mstv
ms.assetid: a071e725-c98d-4061-bda5-d7eca8b4b0e0
ms.date: 12/05/2018
ms.keywords: GetRecordUserNibbles, GetRecordUserNibbles method [Microsoft TV Technologies], GetRecordUserNibbles method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetRecordUserNibbles method, IDvbContentDescriptor.GetRecordUserNibbles, IDvbContentDescriptor::GetRecordUserNibbles, dvbsiparser/IDvbContentDescriptor::GetRecordUserNibbles, mstv.idvbcontentdescriptor_getrecordusernibbles
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
 - IDvbContentDescriptor::GetRecordUserNibbles
 - dvbsiparser/IDvbContentDescriptor::GetRecordUserNibbles
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
 - IDvbContentDescriptor.GetRecordUserNibbles
---

# IDvbContentDescriptor::GetRecordUserNibbles


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the two 4-bit fields that make up a broadcaster-defined identifier for a content descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">IDvbContentDescriptor::GetCountOfRecords</a>

### -param pbVal1 [out]

Gets the most-significant four bits of the broadcaster-defined content identifier. These bits are returned in the  right-most four bits of the byte.

### -param pbVal2 [out]

Gets the least-significant four bits of the broadcaster-defined  content identifier. These bits are returned in the left-most four bits of the byte.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentdescriptor">IDvbContentDescriptor</a>