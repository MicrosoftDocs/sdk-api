---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetRecordItemRawBytes
title: IDvbExtendedEventDescriptor::GetRecordItemRawBytes (dvbsiparser.h)
description: Gets the raw data from the current item in a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetRecordItemRawBytes","GetRecordItemRawBytes method [Microsoft TV Technologies]","GetRecordItemRawBytes method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetRecordItemRawBytes method","IDvbExtendedEventDescriptor.GetRecordItemRawBytes","IDvbExtendedEventDescriptor::GetRecordItemRawBytes","dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemRawBytes","mstv.idvbextendedeventdescriptor_getrecorditemrawbytes"]
old-location: mstv\idvbextendedeventdescriptor_getrecorditemrawbytes.htm
tech.root: mstv
ms.assetid: ed3046ad-b987-479a-a2ba-d761b2d83c86
ms.date: 12/05/2018
ms.keywords: GetRecordItemRawBytes, GetRecordItemRawBytes method [Microsoft TV Technologies], GetRecordItemRawBytes method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetRecordItemRawBytes method, IDvbExtendedEventDescriptor.GetRecordItemRawBytes, IDvbExtendedEventDescriptor::GetRecordItemRawBytes, dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemRawBytes, mstv.idvbextendedeventdescriptor_getrecorditemrawbytes
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
 - IDvbExtendedEventDescriptor::GetRecordItemRawBytes
 - dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemRawBytes
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
 - IDvbExtendedEventDescriptor.GetRecordItemRawBytes
---

# IDvbExtendedEventDescriptor::GetRecordItemRawBytes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the raw data from the 
current item in a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the item record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getcountofrecords">IDvbExtendedEventDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param ppbRawItem [out]

Pointer to a buffer that gets the item data. The caller is responsible for freeing this memory.

### -param pbItemLength [out]

Receives the number of bytes in the item description.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getcountofrecords">IDvbExtendedEventDescriptor::GetCountOfRecords</a>