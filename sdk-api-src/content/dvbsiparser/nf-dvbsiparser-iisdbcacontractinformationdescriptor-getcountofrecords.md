---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetCountOfRecords
title: IIsdbCAContractInformationDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbCAContractInformationDescriptor.GetCountOfRecords","IIsdbCAContractInformationDescriptor::GetCountOfRecords","dvbsiparser/IIsdbCAContractInformationDescriptor::GetCountOfRecords","mstv.iisdbcacontractinformationdescriptor_getcountofrecords"]
old-location: mstv\iisdbcacontractinformationdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 00df3bb9-494b-4e2c-b836-4893fd6eff8c
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbCAContractInformationDescriptor.GetCountOfRecords, IIsdbCAContractInformationDescriptor::GetCountOfRecords, dvbsiparser/IIsdbCAContractInformationDescriptor::GetCountOfRecords, mstv.iisdbcacontractinformationdescriptor_getcountofrecords
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
 - IIsdbCAContractInformationDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbCAContractInformationDescriptor::GetCountOfRecords
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
 - IIsdbCAContractInformationDescriptor.GetCountOfRecords
---

# IIsdbCAContractInformationDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the number of records in an Integrated Services Digital Broadcasting (ISDB)  conditional access (CA) contract information descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>