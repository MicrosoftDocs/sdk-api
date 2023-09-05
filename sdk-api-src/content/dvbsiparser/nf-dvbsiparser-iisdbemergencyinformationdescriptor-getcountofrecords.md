---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetCountOfRecords
title: IIsdbEmergencyInformationDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an emergency information descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbEmergencyInformationDescriptor interface","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbEmergencyInformationDescriptor.GetCountOfRecords","IIsdbEmergencyInformationDescriptor::GetCountOfRecords","dvbsiparser/IIsdbEmergencyInformationDescriptor::GetCountOfRecords","mstv.iisdbemergencyinformationdescriptor_getcountofrecords"]
old-location: mstv\iisdbemergencyinformationdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: d23f1cc0-c6b0-4054-80be-36d7675fdec7
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbEmergencyInformationDescriptor.GetCountOfRecords, IIsdbEmergencyInformationDescriptor::GetCountOfRecords, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetCountOfRecords, mstv.iisdbemergencyinformationdescriptor_getcountofrecords
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
 - IIsdbEmergencyInformationDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbEmergencyInformationDescriptor::GetCountOfRecords
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
 - IIsdbEmergencyInformationDescriptor.GetCountOfRecords
---

# IIsdbEmergencyInformationDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the number of records in an emergency information descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbemergencyinformationdescriptor">IIsdbEmergencyInformationDescriptor</a>