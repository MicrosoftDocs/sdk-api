---
UID: NF:winsxs.IAssemblyName.GetProperty
title: IAssemblyName::GetProperty (winsxs.h)
author: windows-sdk-content
description: The GetProperty method gets the value of a name-value pair in the assembly name.
old-location: setup\iassemblyname_getproperty.htm
tech.root: SbsCs
ms.assetid: 0526fac9-1a3f-403b-b886-a7f833913e18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProperty, GetProperty method [Side-by-side Assemblies], GetProperty method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],GetProperty method, IAssemblyName.GetProperty, IAssemblyName::GetProperty, setup.iassemblyname_getproperty, winsxs/IAssemblyName::GetProperty
ms.topic: method
req.header: winsxs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Sxs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sxs.dll
api_name:
 - IAssemblyName.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAssemblyName::GetProperty


## -description


The <b>GetProperty</b> method gets the value of a name-value pair in the assembly name.


## -parameters




### -param PropertyId [in]

A property ID that represents the name-value pair. Valid property IDs are <a href="https://msdn.microsoft.com/5e13e90e-68b0-4842-97de-4f179d4c9ad7">ASM_NAME</a> enumeration values.


### -param pvProperty [out]

A pointer to a buffer that receives the value of the name-value pair.


### -param pcbProperty [in, out]

The size in bytes of the buffer specified by <i>pvProperty</i>. The value is zero if this property is not set.


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




<a href="https://msdn.microsoft.com/304b8fb3-5d17-4af0-b070-450a40dc5cc9">IAssemblyName</a>
 

 

