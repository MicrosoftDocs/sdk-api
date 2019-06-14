---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetRecordServiceId
title: IDvbServiceListDescriptor::GetRecordServiceId (dvbsiparser.h)
author: windows-sdk-content
description: Gets the value of the service_id field from a Digital Video Broadcast (DVB) service list descriptor.The service_id field value uniquely identifies the service within the MPEG-2 transport stream.
old-location: mstv\idvbservicelistdescriptor_getrecordserviceid.htm
tech.root: mstv
ms.assetid: c98d032a-0a3c-4e27-a5b7-ee594024ac9d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordServiceId, GetRecordServiceId method [Microsoft TV Technologies], GetRecordServiceId method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetRecordServiceId method, IDvbServiceListDescriptor.GetRecordServiceId, IDvbServiceListDescriptor::GetRecordServiceId, dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceId, mstv.idvbservicelistdescriptor_getrecordserviceid
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbServiceListDescriptor.GetRecordServiceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbServiceListDescriptor::GetRecordServiceId


## -description


Gets the value of the service_id field from a Digital Video Broadcast (DVB) service list descriptor.The service_id field value uniquely identifies the service within the MPEG-2 transport stream.


## -parameters




### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">IDvbServiceListDescriptor::GetCountOfRecords</a>method to get the number of records in the logical channel descriptor.


### -param pwVal [out]

Receives the service_id field value. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicelistdescriptor">IDvbServiceListDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">IDvbServiceListDescriptor::GetCountOfRecords</a>
 

 

