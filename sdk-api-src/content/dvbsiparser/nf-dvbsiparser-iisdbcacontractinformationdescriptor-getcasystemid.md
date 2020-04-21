---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetCASystemId
title: IIsdbCAContractInformationDescriptor::GetCASystemId (dvbsiparser.h)
description: Gets the value of the CA_system_id field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field identifies the conditional access system associated with the contract information.helpviewer_keywords: ["GetCASystemId","GetCASystemId method [Microsoft TV Technologies]","GetCASystemId method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetCASystemId method","IIsdbCAContractInformationDescriptor.GetCASystemId","IIsdbCAContractInformationDescriptor::GetCASystemId","dvbsiparser/IIsdbCAContractInformationDescriptor::GetCASystemId","mstv.iisdbcacontractinformationdescriptor_getcasystemid"]
old-location: mstv\iisdbcacontractinformationdescriptor_getcasystemid.htm
tech.root: mstv
ms.assetid: cb9f55c1-7967-43e4-9cb3-1d7cdf20c70a
ms.date: 12/05/2018
ms.keywords: GetCASystemId, GetCASystemId method [Microsoft TV Technologies], GetCASystemId method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetCASystemId method, IIsdbCAContractInformationDescriptor.GetCASystemId, IIsdbCAContractInformationDescriptor::GetCASystemId, dvbsiparser/IIsdbCAContractInformationDescriptor::GetCASystemId, mstv.iisdbcacontractinformationdescriptor_getcasystemid
f1_keywords:
- dvbsiparser/IIsdbCAContractInformationDescriptor.GetCASystemId
dev_langs:
- c++
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
- IIsdbCAContractInformationDescriptor.GetCASystemId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCAContractInformationDescriptor::GetCASystemId


## -description


Gets the value of the CA_system_id field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field identifies the conditional access system associated with the contract information.


## -parameters




### -param pwVal [out]

Receives the conditional access system identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>
 

 

