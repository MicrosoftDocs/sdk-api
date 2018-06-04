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

# ITypeInfo::GetVarDesc


## -description


Retrieves a VARDESC structure that describes the specified variable.


## -parameters




### -param index [in]

The index of the variable whose description is to be returned. The index should be in the range of 0 to 1 less than the number of variables in this type.


### -param ppVarDesc [out]

A VARDESC that describes the specified variable.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



To free the VARDESC structure, use <a href="https://msdn.microsoft.com/a0f734d8-9b14-474a-b701-df8ba7641501">ReleaseVarDesc</a>.



#### Examples

In the following example, the CHECKRESULT function is undefined. Replace this function with your error handling code.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHECKRESULT(ptypeinfo-&gt;GetVarDesc(i, &amp;pvardesc));
idMember = pvardesc-&gt;memid;
CHECKRESULT(ptypeinfo-&gt;GetDocumentation(idMember, &amp;bstrName, NULL, NULL, 
      NULL));
ptypeinfo-&gt;ReleaseVarDesc(pvardesc);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

