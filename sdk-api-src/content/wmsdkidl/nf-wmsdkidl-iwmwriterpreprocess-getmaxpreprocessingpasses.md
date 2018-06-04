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

# IWMWriterPreprocess::GetMaxPreprocessingPasses


## -description



The <b>GetMaxPreprocessingPasses</b> method retrieves the maximum number of preprocessing passes for a specified input stream.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number for which you want to get the maximum number of preprocessing passes.


### -param dwFlags [in]

Reserved. Set to zero.


### -param pdwMaxNumPasses [out]

Pointer to a <b>DWORD</b> that will receive the maximum number of preprocessing passes. If the codec supports two-pass encoding, this value is 1, as the final pass is not counted.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwMaxNumPasses</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNum</i> specifies an invalid input stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is not running.

</td>
</tr>
</table>
 




## -remarks



If no preprocessing is supported for the specified input, <i>pdwMaxNumPasses</i> contains zero upon return.




## -see-also




<a href="https://msdn.microsoft.com/06803639-3f21-4003-a460-16a0b5cc6d6f">IWMWriterPreprocess Interface</a>
 

 

