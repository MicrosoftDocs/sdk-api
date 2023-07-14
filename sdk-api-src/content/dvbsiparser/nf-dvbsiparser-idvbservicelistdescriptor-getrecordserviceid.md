---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetRecordServiceId
title: IDvbServiceListDescriptor::GetRecordServiceId (dvbsiparser.h)
description: Gets the value of the service_id field from a Digital Video Broadcast (DVB) service list descriptor.The service_id field value uniquely identifies the service within the MPEG-2 transport stream.
helpviewer_keywords: ["GetRecordServiceId","GetRecordServiceId method [Microsoft TV Technologies]","GetRecordServiceId method [Microsoft TV Technologies]","IDvbServiceListDescriptor interface","IDvbServiceListDescriptor interface [Microsoft TV Technologies]","GetRecordServiceId method","IDvbServiceListDescriptor.GetRecordServiceId","IDvbServiceListDescriptor::GetRecordServiceId","dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceId","mstv.idvbservicelistdescriptor_getrecordserviceid"]
old-location: mstv\idvbservicelistdescriptor_getrecordserviceid.htm
tech.root: mstv
ms.assetid: c98d032a-0a3c-4e27-a5b7-ee594024ac9d
ms.date: 12/05/2018
ms.keywords: GetRecordServiceId, GetRecordServiceId method [Microsoft TV Technologies], GetRecordServiceId method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetRecordServiceId method, IDvbServiceListDescriptor.GetRecordServiceId, IDvbServiceListDescriptor::GetRecordServiceId, dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceId, mstv.idvbservicelistdescriptor_getrecordserviceid
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
 - IDvbServiceListDescriptor::GetRecordServiceId
 - dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceId
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
 - IDvbServiceListDescriptor.GetRecordServiceId
---

# IDvbServiceListDescriptor::GetRecordServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the service_id field from a Digital Video Broadcast (DVB) service list descriptor.The service_id field value uniquely identifies the service within the MPEG-2 transport stream.

## -parameters

### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">IDvbServiceListDescriptor::GetCountOfRecords</a> method to get the number of records in the logical channel descriptor.

### -param pwVal [out]

Receives the service_id field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicelistdescriptor">IDvbServiceListDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">IDvbServiceListDescriptor::GetCountOfRecords</a>