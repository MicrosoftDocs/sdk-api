---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo
title: IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo (dvbsiparser.h)
description: Gets the transmission_type_info field from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetRecordTransmissionTypeInfo","GetRecordTransmissionTypeInfo method [Microsoft TV Technologies]","GetRecordTransmissionTypeInfo method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetRecordTransmissionTypeInfo method","IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo","IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo","dvbsiparser/IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo","mstv.iisdbtsinformationdescriptor_getrecordtransmissiontypeinfo"]
old-location: mstv\iisdbtsinformationdescriptor_getrecordtransmissiontypeinfo.htm
tech.root: mstv
ms.assetid: 992ef7de-ccf8-42a1-bb83-4b5f396164ce
ms.date: 12/05/2018
ms.keywords: GetRecordTransmissionTypeInfo, GetRecordTransmissionTypeInfo method [Microsoft TV Technologies], GetRecordTransmissionTypeInfo method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRecordTransmissionTypeInfo method, IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo, IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo, dvbsiparser/IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo, mstv.iisdbtsinformationdescriptor_getrecordtransmissiontypeinfo
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
 - IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo
 - dvbsiparser/IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo
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
 - IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo
---

# IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the transmission_type_info field from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. This field is used to select hierarchical layers within the service information and is defined by each service provider.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>

### -param pbVal [out]

Receives the transmission_type_info field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>