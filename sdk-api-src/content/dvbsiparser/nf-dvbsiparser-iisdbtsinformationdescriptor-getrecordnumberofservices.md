---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRecordNumberOfServices
title: IIsdbTSInformationDescriptor::GetRecordNumberOfServices (dvbsiparser.h)
description: Gets the number of service records from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetRecordNumberOfServices","GetRecordNumberOfServices method [Microsoft TV Technologies]","GetRecordNumberOfServices method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetRecordNumberOfServices method","IIsdbTSInformationDescriptor.GetRecordNumberOfServices","IIsdbTSInformationDescriptor::GetRecordNumberOfServices","dvbsiparser/IIsdbTSInformationDescriptor::GetRecordNumberOfServices","mstv.iisdbtsinformationdescriptor_getrecordnumberofservices"]
old-location: mstv\iisdbtsinformationdescriptor_getrecordnumberofservices.htm
tech.root: mstv
ms.assetid: bf9ec856-951e-4a75-a136-9fa6eaf9e8cd
ms.date: 12/05/2018
ms.keywords: GetRecordNumberOfServices, GetRecordNumberOfServices method [Microsoft TV Technologies], GetRecordNumberOfServices method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRecordNumberOfServices method, IIsdbTSInformationDescriptor.GetRecordNumberOfServices, IIsdbTSInformationDescriptor::GetRecordNumberOfServices, dvbsiparser/IIsdbTSInformationDescriptor::GetRecordNumberOfServices, mstv.iisdbtsinformationdescriptor_getrecordnumberofservices
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
 - IIsdbTSInformationDescriptor::GetRecordNumberOfServices
 - dvbsiparser/IIsdbTSInformationDescriptor::GetRecordNumberOfServices
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
 - IIsdbTSInformationDescriptor.GetRecordNumberOfServices
---

# IIsdbTSInformationDescriptor::GetRecordNumberOfServices


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of service records from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>.

### -param pbVal [out]

Receives the number of service records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>