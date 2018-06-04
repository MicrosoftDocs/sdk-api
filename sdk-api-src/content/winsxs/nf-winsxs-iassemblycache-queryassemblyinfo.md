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

# IAssemblyCache::QueryAssemblyInfo


## -description


The <b>QueryAssemblyInfo</b> method queries the side-by-side assembly store for assembly information and validates the files in the side-by-side assembly store against the assembly manifest.


## -parameters




### -param dwFlags [in, optional]

Specifies the information to retrieve.


This parameter can be one or more of the following values or 0.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QUERYASMINFO_FLAG_VALIDATE"></a><a id="queryasminfo_flag_validate"></a><dl>
<dt><b>QUERYASMINFO_FLAG_VALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Validates the assembly files in the side-by-side assembly store against the assembly manifest. This includes the verification of the assembly's hash and strong name signature.

</td>
</tr>
<tr>
<td width="40%"><a id="QUERYASMINFO_FLAG_GETSIZE"></a><a id="queryasminfo_flag_getsize"></a><dl>
<dt><b>QUERYASMINFO_FLAG_GETSIZE</b></dt>
</dl>
</td>
<td width="60%">
Returns the size of all files in the assembly.

</td>
</tr>
</table>
 


### -param pszAssemblyName [in]

Pointer to null-terminated string value containing the fully-specified strong name of the assembly to query. If the name is not fully specified, the result of the method is undefined.


### -param pAsmInfo [in, out]

Pointer to the <a href="https://msdn.microsoft.com/4281b375-0edd-453b-9505-e7dc5bd586fc">ASSEMBLY_INFO</a> structure that receives the information.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c411ae7-5a8f-47ca-a9c1-e23000f64620">IAssemblyCache</a>
 

 

