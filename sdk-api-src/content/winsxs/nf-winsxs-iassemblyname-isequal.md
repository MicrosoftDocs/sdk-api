---
UID: NF:winsxs.IAssemblyName.IsEqual
title: IAssemblyName::IsEqual (winsxs.h)
description: The IsEqual method compares the current assembly name to another assembly name.
helpviewer_keywords: ["IAssemblyName interface [Side-by-side Assemblies]","IsEqual method","IAssemblyName.IsEqual","IAssemblyName::IsEqual","IsEqual","IsEqual method [Side-by-side Assemblies]","IsEqual method [Side-by-side Assemblies]","IAssemblyName interface","setup.iassemblyname_isequal","winsxs/IAssemblyName::IsEqual"]
old-location: setup\iassemblyname_isequal.htm
tech.root: setup
ms.assetid: 798102ce-b696-4940-941d-c3fd3054c584
ms.date: 12/05/2018
ms.keywords: IAssemblyName interface [Side-by-side Assemblies],IsEqual method, IAssemblyName.IsEqual, IAssemblyName::IsEqual, IsEqual, IsEqual method [Side-by-side Assemblies], IsEqual method [Side-by-side Assemblies],IAssemblyName interface, setup.iassemblyname_isequal, winsxs/IAssemblyName::IsEqual
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
 - IAssemblyName::IsEqual
 - winsxs/IAssemblyName::IsEqual
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
 - IAssemblyName.IsEqual
---

# IAssemblyName::IsEqual


## -description

The <b>IsEqual</b> method compares the current assembly name to another assembly name.

## -parameters

### -param pName [in]

A pointer to another  <a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a> instance, which is to be compared to the current assembly.

### -param dwCmpFlags [in]

Indicates which portion of the assembly names are to be compared. The value can be one of the options of the <a href="/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags">ASM_CMP_FLAGS</a> enumeration.

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
The specified portions of the names match.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The specified portions of the names do not match.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a>