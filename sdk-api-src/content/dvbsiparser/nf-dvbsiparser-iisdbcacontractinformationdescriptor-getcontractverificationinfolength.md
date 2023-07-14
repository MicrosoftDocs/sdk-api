---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetContractVerificationInfoLength
title: IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength (dvbsiparser.h)
description: Gets the length of the contract_verification_info field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
helpviewer_keywords: ["GetContractVerificationInfoLength","GetContractVerificationInfoLength method [Microsoft TV Technologies]","GetContractVerificationInfoLength method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetContractVerificationInfoLength method","IIsdbCAContractInformationDescriptor.GetContractVerificationInfoLength","IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength","dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength","mstv.iisdbcacontractinformationdescriptor_getcontractverificationinfolength"]
old-location: mstv\iisdbcacontractinformationdescriptor_getcontractverificationinfolength.htm
tech.root: mstv
ms.assetid: a7000edd-72a1-4979-b603-a42eecc691d7
ms.date: 12/05/2018
ms.keywords: GetContractVerificationInfoLength, GetContractVerificationInfoLength method [Microsoft TV Technologies], GetContractVerificationInfoLength method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetContractVerificationInfoLength method, IIsdbCAContractInformationDescriptor.GetContractVerificationInfoLength, IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength, dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength, mstv.iisdbcacontractinformationdescriptor_getcontractverificationinfolength
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
 - IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength
 - dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength
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
 - IIsdbCAContractInformationDescriptor.GetContractVerificationInfoLength
---

# IIsdbCAContractInformationDescriptor::GetContractVerificationInfoLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of the contract_verification_info field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.

## -parameters

### -param pbVal [out]

Receives the field length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcontractverificationinfo">IIsdbCAContractInformationDescriptor::GetContractVerificationInfo</a>