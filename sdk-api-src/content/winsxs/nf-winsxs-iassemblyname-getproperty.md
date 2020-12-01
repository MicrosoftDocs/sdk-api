---
UID: NF:winsxs.IAssemblyName.GetProperty
title: IAssemblyName::GetProperty (winsxs.h)
description: The GetProperty method gets the value of a name-value pair in the assembly name.
helpviewer_keywords: ["GetProperty","GetProperty method [Side-by-side Assemblies]","GetProperty method [Side-by-side Assemblies]","IAssemblyName interface","IAssemblyName interface [Side-by-side Assemblies]","GetProperty method","IAssemblyName.GetProperty","IAssemblyName::GetProperty","setup.iassemblyname_getproperty","winsxs/IAssemblyName::GetProperty"]
old-location: setup\iassemblyname_getproperty.htm
tech.root: setup
ms.assetid: 0526fac9-1a3f-403b-b886-a7f833913e18
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Side-by-side Assemblies], GetProperty method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],GetProperty method, IAssemblyName.GetProperty, IAssemblyName::GetProperty, setup.iassemblyname_getproperty, winsxs/IAssemblyName::GetProperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAssemblyName::GetProperty
 - winsxs/IAssemblyName::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sxs.dll
api_name:
 - IAssemblyName.GetProperty
---

# IAssemblyName::GetProperty


## -description

The <b>GetProperty</b> method gets the value of a name-value pair in the assembly name.

## -parameters

### -param PropertyId [in]

A property ID that represents the name-value pair. Valid property IDs are <a href="/windows/win32/api/winsxs/ne-winsxs-asm_name">ASM_NAME</a> enumeration values.

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

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a>