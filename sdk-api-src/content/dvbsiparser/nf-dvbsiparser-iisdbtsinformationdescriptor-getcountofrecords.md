---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetCountOfRecords
title: IIsdbTSInformationDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbTSInformationDescriptor.GetCountOfRecords","IIsdbTSInformationDescriptor::GetCountOfRecords","dvbsiparser/IIsdbTSInformationDescriptor::GetCountOfRecords","mstv.iisdbtsinformationdescriptor_getcountofrecords"]
old-location: mstv\iisdbtsinformationdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 97e0d307-f41d-44e3-8f42-d00fecbcd61e
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbTSInformationDescriptor.GetCountOfRecords, IIsdbTSInformationDescriptor::GetCountOfRecords, dvbsiparser/IIsdbTSInformationDescriptor::GetCountOfRecords, mstv.iisdbtsinformationdescriptor_getcountofrecords
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
 - IIsdbTSInformationDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbTSInformationDescriptor::GetCountOfRecords
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
 - IIsdbTSInformationDescriptor.GetCountOfRecords
---

# IIsdbTSInformationDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.

## -parameters

### -param pbVal [out]

Receives the number of descriptor records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>