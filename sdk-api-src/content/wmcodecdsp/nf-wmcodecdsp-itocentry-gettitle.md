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

# ITocEntry::GetTitle


## -description


The <b>GetTitle</b> method retrieves the title, set by a previous call to <a href="https://msdn.microsoft.com/24ab6c56-59ae-4fdf-b18e-75f616ee5a80">SetTitle</a>, of the entry.


## -parameters




### -param pwTitleSize [in, out]

If <i>pwszTitle</i> is <b>NULL</b>, this is an output parameter that receives the size, in wide characters, of the buffer required to receive the title. If <i>pwszTitle</i> is not <b>NULL</b>, this is an input parameter that specifies the size, in wide characters, of the caller-allocated buffer pointed to by <i>pwszTitle</i>.


### -param pwszTitle [out]

<b>NULL</b>, or a pointer to a caller-allocated buffer that, on successful completion, receives the title. The title  is null-terminated.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The method returns this error code if <i>pwszTitle</i> is not <b>NULL</b> and the title, including its NULL terminator, is larger than the size specified by <i>pwTitleSize</i>. In that case, <i>pwTitleSize</i> serves as an output parameter and receives the size of the required buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>



<a href="https://msdn.microsoft.com/24ab6c56-59ae-4fdf-b18e-75f616ee5a80">SetTitle</a>
 

 

