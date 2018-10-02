---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetContractVerificationInfo
title: IIsdbCAContractInformationDescriptor::GetContractVerificationInfo
author: windows-sdk-content
description: Gets data from the contract_verification_info field in an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field is used to determine allowable uses of the conditional access service.
old-location: mstv\iisdbcacontractinformationdescriptor_getcontractverificationinfo.htm
tech.root: MSTV
ms.assetid: bfec246a-df34-46c3-9529-dc1fa75582da
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetContractVerificationInfo, GetContractVerificationInfo method [Microsoft TV Technologies], GetContractVerificationInfo method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetContractVerificationInfo method, IIsdbCAContractInformationDescriptor.GetContractVerificationInfo, IIsdbCAContractInformationDescriptor::GetContractVerificationInfo, dvbsiparser/IIsdbCAContractInformationDescriptor::GetContractVerificationInfo, mstv.iisdbcacontractinformationdescriptor_getcontractverificationinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbCAContractInformationDescriptor.GetContractVerificationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbCAContractInformationDescriptor::GetContractVerificationInfo


## -description


Gets data  from the contract_verification_info field in an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field is used to determine allowable uses of the conditional access service.


## -parameters




### -param bBufLength [in]

Specifies the length of the buffer that holds the contract verification data.


### -param pbBuf [out]

Pointer to a buffer that receives the contract verification data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The contract_verification_info field is used to confirm whether the service, or the ES group
that comprises a service, can be reserved for viewing (recording). When the contract_verification_info field appears in the event information table (EIT), it  is also used to determine whether the event in question is
a flat-type or tier-type event, an ES group that comprises an event, a pay-per-view (PPV) event, or an ES
group that comprises a PPV event. If the event is a PPV event or ES group that comprises a PPV event, the descriptor is used to determine the viewing fee and recording
request information.




## -see-also




<a href="https://msdn.microsoft.com/d877a625-d683-4472-98de-f24c165c753a">IIsdbCAContractInformationDescriptor</a>
 

 

