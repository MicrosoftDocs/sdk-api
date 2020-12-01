---
UID: NF:winsxs.IAssemblyCache.QueryAssemblyInfo
title: IAssemblyCache::QueryAssemblyInfo (winsxs.h)
description: The QueryAssemblyInfo method queries the side-by-side assembly store for assembly information and validates the files in the side-by-side assembly store against the assembly manifest.
helpviewer_keywords: ["IAssemblyCache interface [Side-by-side Assemblies]","QueryAssemblyInfo method","IAssemblyCache.QueryAssemblyInfo","IAssemblyCache::QueryAssemblyInfo","QUERYASMINFO_FLAG_GETSIZE","QUERYASMINFO_FLAG_VALIDATE","QueryAssemblyInfo","QueryAssemblyInfo method [Side-by-side Assemblies]","QueryAssemblyInfo method [Side-by-side Assemblies]","IAssemblyCache interface","setup.iassemblycache_queryassemblyinfo","winsxs/IAssemblyCache::QueryAssemblyInfo"]
old-location: setup\iassemblycache_queryassemblyinfo.htm
tech.root: setup
ms.assetid: fc13e5ac-60cf-43f2-b50e-00be3a1ad270
ms.date: 12/05/2018
ms.keywords: IAssemblyCache interface [Side-by-side Assemblies],QueryAssemblyInfo method, IAssemblyCache.QueryAssemblyInfo, IAssemblyCache::QueryAssemblyInfo, QUERYASMINFO_FLAG_GETSIZE, QUERYASMINFO_FLAG_VALIDATE, QueryAssemblyInfo, QueryAssemblyInfo method [Side-by-side Assemblies], QueryAssemblyInfo method [Side-by-side Assemblies],IAssemblyCache interface, setup.iassemblycache_queryassemblyinfo, winsxs/IAssemblyCache::QueryAssemblyInfo
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
 - IAssemblyCache::QueryAssemblyInfo
 - winsxs/IAssemblyCache::QueryAssemblyInfo
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
 - IAssemblyCache.QueryAssemblyInfo
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

Pointer to the <a href="/windows/desktop/api/winsxs/ns-winsxs-assembly_info">ASSEMBLY_INFO</a> structure that receives the information.

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

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblycache">IAssemblyCache</a>