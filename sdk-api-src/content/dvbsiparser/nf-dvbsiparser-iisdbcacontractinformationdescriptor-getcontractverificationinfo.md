---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetContractVerificationInfo
title: IIsdbCAContractInformationDescriptor::GetContractVerificationInfo (dvbsiparser.h)
description: Gets data from the contract_verification_info field in an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field is used to determine allowable uses of the conditional access service.
helpviewer_keywords: ["GetContractVerificationInfo","GetContractVerificationInfo method [Microsoft TV Technologies]","GetContractVerificationInfo method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetContractVerificationInfo method","IIsdbCAContractInformationDescriptor.GetContractVerificationInfo","IIsdbCAContractInformationDescriptor::GetContractVerificationInfo","dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfo","mstv.iisdbcacontractinformationdescriptor_getcontractverificationinfo"]
old-location: mstv\iisdbcacontractinformationdescriptor_getcontractverificationinfo.htm
tech.root: mstv
ms.assetid: bfec246a-df34-46c3-9529-dc1fa75582da
ms.date: 12/05/2018
ms.keywords: GetContractVerificationInfo, GetContractVerificationInfo method [Microsoft TV Technologies], GetContractVerificationInfo method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetContractVerificationInfo method, IIsdbCAContractInformationDescriptor.GetContractVerificationInfo, IIsdbCAContractInformationDescriptor::GetContractVerificationInfo, dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfo, mstv.iisdbcacontractinformationdescriptor_getcontractverificationinfo
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
 - IIsdbCAContractInformationDescriptor::GetContractVerificationInfo
 - dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfo
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
 - IIsdbCAContractInformationDescriptor.GetContractVerificationInfo
---

# IIsdbCAContractInformationDescriptor::GetContractVerificationInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets data  from the contract_verification_info field in an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field is used to determine allowable uses of the conditional access service.

## -parameters

### -param bBufLength [in]

Specifies the length of the buffer that holds the contract verification data.

### -param pbBuf [out]

Pointer to a buffer that receives the contract verification data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The contract_verification_info field is used to confirm whether the service, or the ES group
that comprises a service, can be reserved for viewing (recording). When the contract_verification_info field appears in the event information table (EIT), it  is also used to determine whether the event in question is
a flat-type or tier-type event, an ES group that comprises an event, a pay-per-view (PPV) event, or an ES
group that comprises a PPV event. If the event is a PPV event or ES group that comprises a PPV event, the descriptor is used to determine the viewing fee and recording
request information.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>