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

# IEnumStreamBufferRecordingAttrib::Next


## -description


The <b>Next</b> method returns a specified number of attributes in the enumeration sequence.


## -parameters




### -param cRequest [in]

The number of attributes to retrieve.


### -param pStreamBufferAttribute [in, out]

Pointer to an array of size <i>cRequest</i>. The array is filled with <a href="https://msdn.microsoft.com/2b17626a-9268-4192-8acf-ed46bf632163">STREAMBUFFER_ATTRIBUTE</a> structures.


### -param pcReceived [out]

Pointer to a variable that receives the number of attributes that are returned in the <i>pStreamBufferAttribute</i> array. This parameter can be <b>NULL</b> if <i>cRequest</i> is 1.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Did not retrieve as many attributes as requested (reached the end of the enumeration).

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
 




## -remarks



The caller allocates the array of <a href="https://msdn.microsoft.com/2b17626a-9268-4192-8acf-ed46bf632163">STREAMBUFFER_ATTRIBUTE</a> structures, but the method allocates buffers for the attributes and the attribute names, which are contained in the <b>pszName</b> and <b>pbAttribute</b> members of each structure. The caller must release those buffers, by calling <b>CoTaskMemFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/668d2e04-74fa-41d7-b238-ec737a4441ca">IEnumStreamBufferRecordingAttrib Interface</a>
 

 

