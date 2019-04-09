---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetRecordComponentTag
title: IIsdbCAContractInformationDescriptor::GetRecordComponentTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the broadcaster-defined tag that identifies a component record from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
old-location: mstv\iisdbcacontractinformationdescriptor_getrecordcomponenttag.htm
tech.root: mstv
ms.assetid: cd032a24-228a-47e3-97f4-1046b426c587
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordComponentTag, GetRecordComponentTag method [Microsoft TV Technologies], GetRecordComponentTag method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetRecordComponentTag method, IIsdbCAContractInformationDescriptor.GetRecordComponentTag, IIsdbCAContractInformationDescriptor::GetRecordComponentTag, dvbsiparser/IIsdbCAContractInformationDescriptor::GetRecordComponentTag, mstv.iisdbcacontractinformationdescriptor_getrecordcomponenttag
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
 - IIsdbCAContractInformationDescriptor.GetRecordComponentTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbCAContractInformationDescriptor::GetRecordComponentTag


## -description


Gets the broadcaster-defined tag that identifies a component record from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the component record that contains the tag. To get the number of components, call <a href="https://msdn.microsoft.com/00df3bb9-494b-4e2c-b836-4893fd6eff8c">IIsdbCAContractInformationDescriptor::GetCountOfRecords</a>.


### -param pbVal [out]

Receives the component record ID tag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d877a625-d683-4472-98de-f24c165c753a">IIsdbCAContractInformationDescriptor</a>
 

 

