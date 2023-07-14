---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRecordServiceIdByIndex
title: IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex (dvbsiparser.h)
description: Gets a service identifier from a specified service record in an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetRecordServiceIdByIndex","GetRecordServiceIdByIndex method [Microsoft TV Technologies]","GetRecordServiceIdByIndex method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetRecordServiceIdByIndex method","IIsdbTSInformationDescriptor.GetRecordServiceIdByIndex","IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex","dvbsiparser/IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex","mstv.iisdbtsinformationdescriptor_getrecordserviceidbyindex"]
old-location: mstv\iisdbtsinformationdescriptor_getrecordserviceidbyindex.htm
tech.root: mstv
ms.assetid: 40738938-226d-4220-8092-a029bd6c038d
ms.date: 12/05/2018
ms.keywords: GetRecordServiceIdByIndex, GetRecordServiceIdByIndex method [Microsoft TV Technologies], GetRecordServiceIdByIndex method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRecordServiceIdByIndex method, IIsdbTSInformationDescriptor.GetRecordServiceIdByIndex, IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex, dvbsiparser/IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex, mstv.iisdbtsinformationdescriptor_getrecordserviceidbyindex
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex
 - dvbsiparser/IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex
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
 - IIsdbTSInformationDescriptor.GetRecordServiceIdByIndex
---

# IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a service identifier from a specified service record in an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>.

### -param bServiceIndex [in]

Zero-based index of the service identifier to return. To get the number of identifiers, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getrecordnumberofservices">IIsdbTSInformationDescriptor::GetRecordNumberOfServices</a>.

### -param pdwVal [out]

Receives the service identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getrecordnumberofservices">IIsdbTSInformationDescriptor::GetRecordNumberOfServices</a>