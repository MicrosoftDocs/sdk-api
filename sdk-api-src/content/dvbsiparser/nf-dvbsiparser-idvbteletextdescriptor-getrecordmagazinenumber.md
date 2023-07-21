---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetRecordMagazineNumber
title: IDvbTeletextDescriptor::GetRecordMagazineNumber (dvbsiparser.h)
description: Gets the magazine number from a Digital Video Broadcast (DVB) teletext descriptor.
helpviewer_keywords: ["GetRecordMagazineNumber","GetRecordMagazineNumber method [Microsoft TV Technologies]","GetRecordMagazineNumber method [Microsoft TV Technologies]","IDvbTeletextDescriptor interface","IDvbTeletextDescriptor interface [Microsoft TV Technologies]","GetRecordMagazineNumber method","IDvbTeletextDescriptor.GetRecordMagazineNumber","IDvbTeletextDescriptor::GetRecordMagazineNumber","dvbsiparser/IDvbTeletextDescriptor::GetRecordMagazineNumber","mstv.idvbteletextdescriptor_getrecordmagazinenumber"]
old-location: mstv\idvbteletextdescriptor_getrecordmagazinenumber.htm
tech.root: mstv
ms.assetid: bb3c39b6-dc85-42ca-9d4b-ad27eae077dd
ms.date: 12/05/2018
ms.keywords: GetRecordMagazineNumber, GetRecordMagazineNumber method [Microsoft TV Technologies], GetRecordMagazineNumber method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetRecordMagazineNumber method, IDvbTeletextDescriptor.GetRecordMagazineNumber, IDvbTeletextDescriptor::GetRecordMagazineNumber, dvbsiparser/IDvbTeletextDescriptor::GetRecordMagazineNumber, mstv.idvbteletextdescriptor_getrecordmagazinenumber
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
 - IDvbTeletextDescriptor::GetRecordMagazineNumber
 - dvbsiparser/IDvbTeletextDescriptor::GetRecordMagazineNumber
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
 - IDvbTeletextDescriptor.GetRecordMagazineNumber
---

# IDvbTeletextDescriptor::GetRecordMagazineNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the magazine number from a Digital Video Broadcast (DVB) teletext descriptor.
  A <i>magazine</i> is a sequence of one or more pages in an enhanced-teletext packet that are normally repeatedly transmitted in numerical sequence

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call 
  <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">IDvbTeletextDescriptor::GetCountOfRecords
</a>.

### -param pbVal [out]

Receives the magazine number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbteletextdescriptor">IDvbTeletextDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">IDvbTeletextDescriptor::GetCountOfRecords
</a>