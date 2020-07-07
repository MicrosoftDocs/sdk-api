---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetTag
title: IIsdbCAContractInformationDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) conditional access (CA)contract information descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbCAContractInformationDescriptor.GetTag","IIsdbCAContractInformationDescriptor::GetTag","dvbsiparser/IIsdbCAContractInformationDescriptor::GetTag","mstv.iisdbcacontractinformationdescriptor_gettag"]
old-location: mstv\iisdbcacontractinformationdescriptor_gettag.htm
tech.root: mstv
ms.assetid: f64110eb-1f96-421c-8f32-3d82a5ed4378
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbCAContractInformationDescriptor.GetTag, IIsdbCAContractInformationDescriptor::GetTag, dvbsiparser/IIsdbCAContractInformationDescriptor::GetTag, mstv.iisdbcacontractinformationdescriptor_gettag
f1_keywords:
- dvbsiparser/IIsdbCAContractInformationDescriptor.GetTag
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
- IIsdbCAContractInformationDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCAContractInformationDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) conditional access (CA)contract information descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB CA contract information descriptors, this value is 0xCB.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>
 

 

