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

# SafeArrayAllocDescriptorEx function


## -description


Creates a safe array descriptor for an array of any valid variant type, including VT_RECORD, without allocating the array data.


## -parameters




### -param vt [in]

The variant type.


### -param cDims [in]

The number of dimensions in the array.


### -param ppsaOut [out]

The safe array descriptor.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> was not valid.

</td>
</tr>
</table>
 




## -remarks



Because <a href="https://msdn.microsoft.com/8fe5c802-cdc0-4e7a-9410-ba65f9a5140e">SafeArrayAllocDescriptor</a> does not take a VARTYPE, it is not possible to use it to create the safe array descriptor for an array of records. The <b>SafeArrayAllocDescriptorEx</b> is used to allocate a safe array descriptor for an array of records of the given dimensions.



