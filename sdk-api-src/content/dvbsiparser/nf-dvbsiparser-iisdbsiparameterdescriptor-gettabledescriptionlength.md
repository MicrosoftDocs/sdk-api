---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTableDescriptionLength
title: IIsdbSIParameterDescriptor::GetTableDescriptionLength
author: windows-sdk-content
description: Gets the body length of a table descriptor in a service information (SI) parameter descriptor.
old-location: mstv\iisdbsiparameterdescriptor_gettabledescriptionlength.htm
tech.root: mstv
ms.assetid: 3dc78381-ac39-4e88-bfe2-bfb91c993576
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTableDescriptionLength, GetTableDescriptionLength method [Microsoft TV Technologies], GetTableDescriptionLength method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTableDescriptionLength method, IIsdbSIParameterDescriptor.GetTableDescriptionLength, IIsdbSIParameterDescriptor::GetTableDescriptionLength, dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionLength, mstv.iisdbsiparameterdescriptor_gettabledescriptionlength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IIsdbSIParameterDescriptor.GetTableDescriptionLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbSIParameterDescriptor::GetTableDescriptionLength


## -description


Gets the body length of a table descriptor in a service information (SI) parameter descriptor. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the SI table descriptor. To get the number of table descriptors, call the <a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a> method.


### -param pbVal [out]

Receives the length of the table descriptor, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/264ae78d-cd72-49ff-b99b-2af637cc2917">IIsdbSIParameterDescriptor</a>



<a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a>
 

 

