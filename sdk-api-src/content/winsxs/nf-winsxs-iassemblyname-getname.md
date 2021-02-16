---
UID: NF:winsxs.IAssemblyName.GetName
title: IAssemblyName::GetName (winsxs.h)
description: The GetName method returns the name portion of the assembly name.
helpviewer_keywords: ["GetName","GetName method [Side-by-side Assemblies]","GetName method [Side-by-side Assemblies]","IAssemblyName interface","IAssemblyName interface [Side-by-side Assemblies]","GetName method","IAssemblyName.GetName","IAssemblyName::GetName","setup.iassemblyname_getname","winsxs/IAssemblyName::GetName"]
old-location: setup\iassemblyname_getname.htm
tech.root: setup
ms.assetid: b27ebe4e-02b6-473f-a8cb-c68a3e65e493
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Side-by-side Assemblies], GetName method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],GetName method, IAssemblyName.GetName, IAssemblyName::GetName, setup.iassemblyname_getname, winsxs/IAssemblyName::GetName
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
 - IAssemblyName::GetName
 - winsxs/IAssemblyName::GetName
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
 - IAssemblyName.GetName
---

# IAssemblyName::GetName


## -description

The <b>GetName</b> method returns the name portion of the assembly name.

## -parameters

### -param lpcwBuffer [in, out]

When calling this method, set this parameter to the size of the buffer specified by <i>pwzName</i>. The specify the size in characters and include the null terminator. When the method returns, the value of <i>lpcwBuffer</i> is the size of the name returned.

### -param pwzName [out]

Pointer to the string value that receives  the name.

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

## -remarks

This method is equivalent to using the <a href="/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getproperty">GetProperty</a> method with the <i>PropertyId</i> set to the <b>ASM_NAME_NAME</b> option of <a href="/windows/win32/api/winsxs/ne-winsxs-asm_name">ASM_NAME</a>. In case ASM_NAME_NAME is not set, the size of the buffer returned by <i>lpcwBuffer</i> is  0, and the content of <i>pwzName</i> is undefined.

## -see-also

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a>