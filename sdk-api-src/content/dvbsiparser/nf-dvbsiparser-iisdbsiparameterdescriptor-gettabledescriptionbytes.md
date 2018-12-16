---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTableDescriptionBytes
title: IIsdbSIParameterDescriptor::GetTableDescriptionBytes
author: windows-sdk-content
description: Gets description data from a table descriptor in a service information (SI) parameter descriptor.
old-location: mstv\iisdbsiparameterdescriptor_gettabledescriptionbytes.htm
tech.root: mstv
ms.assetid: dd73b221-b7b5-43c8-bbdf-f1ea559a0a4e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTableDescriptionBytes, GetTableDescriptionBytes method [Microsoft TV Technologies], GetTableDescriptionBytes method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTableDescriptionBytes method, IIsdbSIParameterDescriptor.GetTableDescriptionBytes, IIsdbSIParameterDescriptor::GetTableDescriptionBytes, dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionBytes, mstv.iisdbsiparameterdescriptor_gettabledescriptionbytes
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
 - IIsdbSIParameterDescriptor.GetTableDescriptionBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbSIParameterDescriptor::GetTableDescriptionBytes


## -description


Gets description data from a table descriptor in a service information (SI) parameter descriptor. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the SI table descriptor. To get the number of table descriptors, call the <a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a> method.


### -param pbBufferLength [in, out]

On input specifies the length of the table descriptor data that is retrieved, in bytes. On output returns the actual data length.


### -param pbBuffer [out]

Receives the table descriptor data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/264ae78d-cd72-49ff-b99b-2af637cc2917">IIsdbSIParameterDescriptor</a>



<a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a>
 

 

