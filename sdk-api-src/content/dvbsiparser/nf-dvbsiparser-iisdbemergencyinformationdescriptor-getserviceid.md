---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetServiceId
title: IIsdbEmergencyInformationDescriptor::GetServiceId (dvbsiparser.h)
description: Gets the identifier for a broadcasting event from an emergency information descriptor.
helpviewer_keywords: ["GetServiceId","GetServiceId method [Microsoft TV Technologies]","GetServiceId method [Microsoft TV Technologies]","IIsdbEmergencyInformationDescriptor interface","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","GetServiceId method","IIsdbEmergencyInformationDescriptor.GetServiceId","IIsdbEmergencyInformationDescriptor::GetServiceId","dvbsiparser/IIsdbEmergencyInformationDescriptor::GetServiceId","mstv.iisdbemergencyinformationdescriptor_getserviceid"]
old-location: mstv\iisdbemergencyinformationdescriptor_getserviceid.htm
tech.root: mstv
ms.assetid: 298f0637-eea1-4247-a9ff-cbe1a82fb8f6
ms.date: 12/05/2018
ms.keywords: GetServiceId, GetServiceId method [Microsoft TV Technologies], GetServiceId method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetServiceId method, IIsdbEmergencyInformationDescriptor.GetServiceId, IIsdbEmergencyInformationDescriptor::GetServiceId, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetServiceId, mstv.iisdbemergencyinformationdescriptor_getserviceid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbEmergencyInformationDescriptor::GetServiceId
 - dvbsiparser/IIsdbEmergencyInformationDescriptor::GetServiceId
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
 - IIsdbEmergencyInformationDescriptor.GetServiceId
---

# IIsdbEmergencyInformationDescriptor::GetServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the identifier for a broadcasting event from an  emergency information descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the emergency information descriptor that contains the event identifiers. To get the number of emergency information descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>

### -param pwVal [out]

Receives the broadcasting event identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbemergencyinformationdescriptor">IIsdbEmergencyInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>