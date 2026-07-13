---
UID: NF:winsxs.IAssemblyName.Finalize
title: IAssemblyName::Finalize (winsxs.h)
description: The Finalize method prevents a side-by-side assembly name from being changed. After Finalize is called, additional calls to the SetProperty returns E_UNEXPECTED.
helpviewer_keywords: ["Finalize","Finalize method [Side-by-side Assemblies]","Finalize method [Side-by-side Assemblies]","IAssemblyName interface","IAssemblyName interface [Side-by-side Assemblies]","Finalize method","IAssemblyName.Finalize","IAssemblyName::Finalize","setup.iassemblyname_finalize","winsxs/IAssemblyName::Finalize"]
old-location: setup\iassemblyname_finalize.htm
tech.root: setup
ms.assetid: 9930826e-3082-4ad3-991e-13cf426983a4
ms.date: 12/05/2018
ms.keywords: Finalize, Finalize method [Side-by-side Assemblies], Finalize method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],Finalize method, IAssemblyName.Finalize, IAssemblyName::Finalize, setup.iassemblyname_finalize, winsxs/IAssemblyName::Finalize
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
 - IAssemblyName::Finalize
 - winsxs/IAssemblyName::Finalize
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
 - IAssemblyName.Finalize
---

# IAssemblyName::Finalize


## -description

The <b>Finalize</b> method prevents a side-by-side  assembly name from being changed. After <b>Finalize</b> is called, additional calls to the <a href="/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-setproperty">SetProperty</a> returns <b>E_UNEXPECTED</b>.



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
