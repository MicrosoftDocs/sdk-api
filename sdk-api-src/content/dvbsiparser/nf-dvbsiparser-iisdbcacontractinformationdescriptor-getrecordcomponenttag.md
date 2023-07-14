---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetRecordComponentTag
title: IIsdbCAContractInformationDescriptor::GetRecordComponentTag (dvbsiparser.h)
description: Gets the broadcaster-defined tag that identifies a component record from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
helpviewer_keywords: ["GetRecordComponentTag","GetRecordComponentTag method [Microsoft TV Technologies]","GetRecordComponentTag method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetRecordComponentTag method","IIsdbCAContractInformationDescriptor.GetRecordComponentTag","IIsdbCAContractInformationDescriptor::GetRecordComponentTag","dvbsiparser/IIsdbCAContractInformationDescriptor::GetRecordComponentTag","mstv.iisdbcacontractinformationdescriptor_getrecordcomponenttag"]
old-location: mstv\iisdbcacontractinformationdescriptor_getrecordcomponenttag.htm
tech.root: mstv
ms.assetid: cd032a24-228a-47e3-97f4-1046b426c587
ms.date: 12/05/2018
ms.keywords: GetRecordComponentTag, GetRecordComponentTag method [Microsoft TV Technologies], GetRecordComponentTag method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetRecordComponentTag method, IIsdbCAContractInformationDescriptor.GetRecordComponentTag, IIsdbCAContractInformationDescriptor::GetRecordComponentTag, dvbsiparser/IIsdbCAContractInformationDescriptor::GetRecordComponentTag, mstv.iisdbcacontractinformationdescriptor_getrecordcomponenttag
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
 - IIsdbCAContractInformationDescriptor::GetRecordComponentTag
 - dvbsiparser/IIsdbCAContractInformationDescriptor::GetRecordComponentTag
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
 - IIsdbCAContractInformationDescriptor.GetRecordComponentTag
---

# IIsdbCAContractInformationDescriptor::GetRecordComponentTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the broadcaster-defined tag that identifies a component record from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the component record that contains the tag. To get the number of components, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcountofrecords">IIsdbCAContractInformationDescriptor::GetCountOfRecords</a>.

### -param pbVal [out]

Receives the component record ID tag.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>