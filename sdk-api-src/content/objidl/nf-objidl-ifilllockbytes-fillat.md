---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFillLockBytes::FillAt


## -description



			The 
<b>FillAt</b> method writes a new block of data to a specified location in the byte array.


## -parameters




### -param ulOffset




### -param pv [in]

Pointer to the data to be written at the location specified by <i>uIOffset</i>.


### -param cb [in]

Size of <i>pv</i> in bytes.


### -param pcbWritten [out]

Number of bytes that were successfully written.


#### - uIOffset [in]

The offset, expressed in number of bytes, from the first element of the byte array.


## -returns




						This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL in addition to the following:




## -remarks



The 
<b>FillAt</b> method is used for nonsequential downloading (for example, HTTP byte range requests). In nonsequential downloading the caller specifies ranges in the byte array where various blocks of data are to be written. Subsequent calls by the compound file implementation to <a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a> are passed by the byte array wrapper object's own implementation of 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> to the underlying byte array. This method is not currently implemented and will return E_NOTIMPL.

<div class="alert"><b>Note</b>  The system-supplied 
<a href="https://msdn.microsoft.com/a8aed8c5-3c4c-4cce-b568-68031da0edf5">IFillLockBytes</a> implementation does not support 
<b>FillAt</b> and returns E_NOTIMPL.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a8aed8c5-3c4c-4cce-b568-68031da0edf5">IFillLockBytes - Implementation</a>



<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a>



<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a>
 

 

