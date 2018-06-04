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

# IMultiMediaStream::GetInformation


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetInformation</code> method retrieves the capabilities of the multimedia stream object.




## -parameters




### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MMSSF_ASYNCHRONOUS</td>
<td>The object supports asynchronous sample updates. This flag is always returned.</td>
</tr>
<tr>
<td>MMSSF_HASCLOCK</td>
<td>The object has a clock.</td>
</tr>
<tr>
<td>MMSSF_SUPPORTSEEK</td>
<td>The object supports seeking.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.


### -param pStreamType [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/07ab5ded-28b8-4cac-b4da-76f07ad351ef">STREAM_TYPE</a> enumeration. This value indicates whether the multimedia stream is read-only, write-only, or read/write. This parameter can be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

