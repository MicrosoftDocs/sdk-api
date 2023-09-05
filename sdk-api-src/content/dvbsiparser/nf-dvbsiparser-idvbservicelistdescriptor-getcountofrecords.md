---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetCountOfRecords
title: IDvbServiceListDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets an indexed count of service records for a Digital Video Broadcast (DVB) service list descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDvbServiceListDescriptor interface","IDvbServiceListDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IDvbServiceListDescriptor.GetCountOfRecords","IDvbServiceListDescriptor::GetCountOfRecords","dvbsiparser/IDvbServiceListDescriptor::GetCountOfRecords","mstv.idvbservicelistdescriptor_getcountofrecords"]
old-location: mstv\idvbservicelistdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 8a3dd6b9-a7a1-49fd-806d-05c726bbe99e
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbServiceListDescriptor.GetCountOfRecords, IDvbServiceListDescriptor::GetCountOfRecords, dvbsiparser/IDvbServiceListDescriptor::GetCountOfRecords, mstv.idvbservicelistdescriptor_getcountofrecords
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
 - IDvbServiceListDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbServiceListDescriptor::GetCountOfRecords
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
 - IDvbServiceListDescriptor.GetCountOfRecords
---

# IDvbServiceListDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an indexed count of service records for a Digital Video Broadcast (DVB) service list descriptor.

## -parameters

### -param pbVal [out]

Receives the number of service records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicelistdescriptor">IDvbServiceListDescriptor</a>