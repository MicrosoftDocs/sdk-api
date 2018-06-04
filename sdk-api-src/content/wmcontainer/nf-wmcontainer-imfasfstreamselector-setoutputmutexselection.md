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

# IMFASFStreamSelector::SetOutputMutexSelection


## -description



Selects a mutual exclusion record to use for a mutual exclusion object associated with an output.




## -parameters




### -param dwOutputNum [in]

The output number for which to set a stream.


### -param dwMutexNum [in]

Index of the mutual exclusion for which to select.


### -param wSelectedRecord [in]

Record of the specified mutual exclusion to select.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



An output is a stream in an Advanced Systems Format (ASF) data section that will be parsed. If mutual exclusion is used, mutually exclusive streams share the same output.

An ASF file can contain multiple mutually exclusive relationships, such as a file with both language based and bit-rate based mutual exclusion. If an output is involved in multiple mutually exclusive relationships, a record from each must be selected.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>



<a href="https://msdn.microsoft.com/d134f4a9-9bca-454f-8dc1-2e152684a4bf">IMFASFStreamSelector::GetOutputMutex</a>
 

 

