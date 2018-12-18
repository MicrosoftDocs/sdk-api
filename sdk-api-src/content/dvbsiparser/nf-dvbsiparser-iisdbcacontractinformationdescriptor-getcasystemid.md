---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetCASystemId
title: IIsdbCAContractInformationDescriptor::GetCASystemId
author: windows-sdk-content
description: Gets the value of the CA_system_id field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field identifies the conditional access system associated with the contract information.
old-location: mstv\iisdbcacontractinformationdescriptor_getcasystemid.htm
tech.root: mstv
ms.assetid: cb9f55c1-7967-43e4-9cb3-1d7cdf20c70a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCASystemId, GetCASystemId method [Microsoft TV Technologies], GetCASystemId method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetCASystemId method, IIsdbCAContractInformationDescriptor.GetCASystemId, IIsdbCAContractInformationDescriptor::GetCASystemId, dvbsiparser/IIsdbCAContractInformationDescriptor::GetCASystemId, mstv.iisdbcacontractinformationdescriptor_getcasystemid
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
 - IIsdbCAContractInformationDescriptor.GetCASystemId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/d877a625-d683-4472-98de-f24c165c753a">IIsdbCAContractInformationDescriptor</a>
 

 

