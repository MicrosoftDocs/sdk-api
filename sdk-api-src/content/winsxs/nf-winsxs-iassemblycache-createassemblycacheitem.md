---
UID: NF:winsxs.IAssemblyCache.CreateAssemblyCacheItem
title: IAssemblyCache::CreateAssemblyCacheItem (winsxs.h)
description: The CreateAssemblyCacheItem method creates an item in the assembly cache that corresponds to the side-by-side assembly being installed.
helpviewer_keywords: ["CreateAssemblyCacheItem","CreateAssemblyCacheItem method [Side-by-side Assemblies]","CreateAssemblyCacheItem method [Side-by-side Assemblies]","IAssemblyCache interface","IAssemblyCache interface [Side-by-side Assemblies]","CreateAssemblyCacheItem method","IAssemblyCache.CreateAssemblyCacheItem","IAssemblyCache::CreateAssemblyCacheItem","setup.iassemblycache_createassemblycacheitem","winsxs/IAssemblyCache::CreateAssemblyCacheItem"]
old-location: setup\iassemblycache_createassemblycacheitem.htm
tech.root: setup
ms.assetid: f88b688c-b349-43e4-aec0-90e064dc2b87
ms.date: 12/05/2018
ms.keywords: CreateAssemblyCacheItem, CreateAssemblyCacheItem method [Side-by-side Assemblies], CreateAssemblyCacheItem method [Side-by-side Assemblies],IAssemblyCache interface, IAssemblyCache interface [Side-by-side Assemblies],CreateAssemblyCacheItem method, IAssemblyCache.CreateAssemblyCacheItem, IAssemblyCache::CreateAssemblyCacheItem, setup.iassemblycache_createassemblycacheitem, winsxs/IAssemblyCache::CreateAssemblyCacheItem
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
 - IAssemblyCache::CreateAssemblyCacheItem
 - winsxs/IAssemblyCache::CreateAssemblyCacheItem
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
 - IAssemblyCache.CreateAssemblyCacheItem
---

# IAssemblyCache::CreateAssemblyCacheItem


## -description

The <b>CreateAssemblyCacheItem</b> method creates an item in the assembly cache that corresponds to the side-by-side assembly being installed.

## -parameters

### -param dwFlags [in]

Reserved.

### -param pvReserved [in]

Reserved.

### -param ppAsmItem [out]

Pointer to a location containing the pointer to the instance of the <a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblycacheitem">IAssemblyCacheItem</a> that receives the information.

### -param pszAssemblyName [in, optional]

Pointer to a null-terminated string value containing the fully-specified strong name of the assembly that is being installed. The name provided is verified to match the name of the assembly in the manifest. Partial names return <b>FUSION_E_INVALID_NAME</b>. If this parameter is null, the name is not verified.

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
<tr>
<td width="40%">
<dl>
<dt>FUSION_E_INVALID_NAME</dt>
</dl>
</td>
<td width="60%">
The full name of the assembly must be provided by <i>pszAssemblyName</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblycache">IAssemblyCache</a>