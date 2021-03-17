---
UID: NF:winsxs.IAssemblyName.GetDisplayName
title: IAssemblyName::GetDisplayName (winsxs.h)
description: The GetDisplayName method gets a string representation of the side-by-side assembly name.
helpviewer_keywords: ["GetDisplayName","GetDisplayName method [Side-by-side Assemblies]","GetDisplayName method [Side-by-side Assemblies]","IAssemblyName interface","IAssemblyName interface [Side-by-side Assemblies]","GetDisplayName method","IAssemblyName.GetDisplayName","IAssemblyName::GetDisplayName","setup.iassemblyname_getdisplayname","winsxs/IAssemblyName::GetDisplayName"]
old-location: setup\iassemblyname_getdisplayname.htm
tech.root: setup
ms.assetid: d2d74d67-a893-4f2f-8161-80bf3d5cbedb
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [Side-by-side Assemblies], GetDisplayName method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],GetDisplayName method, IAssemblyName.GetDisplayName, IAssemblyName::GetDisplayName, setup.iassemblyname_getdisplayname, winsxs/IAssemblyName::GetDisplayName
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
 - IAssemblyName::GetDisplayName
 - winsxs/IAssemblyName::GetDisplayName
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
 - IAssemblyName.GetDisplayName
---

# IAssemblyName::GetDisplayName


## -description

The <b>GetDisplayName</b> method gets a string representation of the side-by-side assembly name.

## -parameters

### -param szDisplayName [out]

A pointer to a buffer that receives the string value that contains the assembly name.

### -param pccDisplayName [in, out]

When calling this method, set this parameter to the size of the buffer specified by <b>szDisplayName</b>. Specify the size in characters and include the null terminator. When the method returns, the value of <i>pccDisplayName</i> is the size of the name returned.

### -param dwDisplayFlags [in]

One or more of the options of the <a href="/windows/win32/api/winsxs/ne-winsxs-asm_display_flags">ASM_DISPLAY_FLAGS</a> enumeration to specify which portions of the assembly's name to include in the string representation of the assembly name. The default for <i>dwDisplayFlags</i> is 0, which returns all portions of the assembly's display name.

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