---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetTag
title: IIsdbCAContractInformationDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) conditional access (CA)contract information descriptor.
old-location: mstv\iisdbcacontractinformationdescriptor_gettag.htm
tech.root: mstv
ms.assetid: f64110eb-1f96-421c-8f32-3d82a5ed4378
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbCAContractInformationDescriptor.GetTag, IIsdbCAContractInformationDescriptor::GetTag, dvbsiparser/IIsdbCAContractInformationDescriptor::GetTag, mstv.iisdbcacontractinformationdescriptor_gettag
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
 - IIsdbCAContractInformationDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/d877a625-d683-4472-98de-f24c165c753a">IIsdbCAContractInformationDescriptor</a>
 

 

