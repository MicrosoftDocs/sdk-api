---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetCountOfRecords
title: IDvbTeletextDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of service records in a Digital Video Broadcast (DVB) teletext descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbTeletextDescriptor interface","IDvbTeletextDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbTeletextDescriptor.GetCountOfRecords","IDvbTeletextDescriptor::GetCountOfRecords","dvbsiparser/IDvbTeletextDescriptor::GetCountOfRecords","mstv.idvbteletextdescriptor_getcountofrecords"]
old-location: mstv\idvbteletextdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: a802c685-9d7a-446a-a29c-4fc3e9ad3dc4
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbTeletextDescriptor.GetCountOfRecords, IDvbTeletextDescriptor::GetCountOfRecords, dvbsiparser/IDvbTeletextDescriptor::GetCountOfRecords, mstv.idvbteletextdescriptor_getcountofrecords
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
 - IDvbTeletextDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbTeletextDescriptor::GetCountOfRecords
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
 - IDvbTeletextDescriptor.GetCountOfRecords
---

# IDvbTeletextDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of service records in a Digital Video Broadcast (DVB) teletext descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records in the teletext descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbteletextdescriptor">IDvbTeletextDescriptor</a>