---
UID: NF:winsxs.IAssemblyCache.UninstallAssembly
title: IAssemblyCache::UninstallAssembly (winsxs.h)
description: The UnistallAssembly method removes an application reference to an assembly from the side-by-side store.
helpviewer_keywords: ["IASSEMBLYCACHE_UNINSTALL_DISPOSITION_ALREADY_UNINSTALLED","IASSEMBLYCACHE_UNINSTALL_DISPOSITION_DELETE_PENDING","IASSEMBLYCACHE_UNINSTALL_DISPOSITION_HAS_INSTALL_REFERENCES","IASSEMBLYCACHE_UNINSTALL_DISPOSITION_REFERENCE_NOT_FOUND","IASSEMBLYCACHE_UNINSTALL_DISPOSITION_STILL_IN_USE","IASSEMBLYCACHE_UNINSTALL_DISPOSITION_UNINSTALLED","IAssemblyCache interface [Side-by-side Assemblies]","UninstallAssembly method","IAssemblyCache.UninstallAssembly","IAssemblyCache::UninstallAssembly","UninstallAssembly","UninstallAssembly method [Side-by-side Assemblies]","UninstallAssembly method [Side-by-side Assemblies]","IAssemblyCache interface","setup.iassemblycache_uninstallassembly","winsxs/IAssemblyCache::UninstallAssembly"]
old-location: setup\iassemblycache_uninstallassembly.htm
tech.root: setup
ms.assetid: b492e93c-73f2-4d68-ae1a-c82e9ec36a72
ms.date: 12/05/2018
ms.keywords: IASSEMBLYCACHE_UNINSTALL_DISPOSITION_ALREADY_UNINSTALLED, IASSEMBLYCACHE_UNINSTALL_DISPOSITION_DELETE_PENDING, IASSEMBLYCACHE_UNINSTALL_DISPOSITION_HAS_INSTALL_REFERENCES, IASSEMBLYCACHE_UNINSTALL_DISPOSITION_REFERENCE_NOT_FOUND, IASSEMBLYCACHE_UNINSTALL_DISPOSITION_STILL_IN_USE, IASSEMBLYCACHE_UNINSTALL_DISPOSITION_UNINSTALLED, IAssemblyCache interface [Side-by-side Assemblies],UninstallAssembly method, IAssemblyCache.UninstallAssembly, IAssemblyCache::UninstallAssembly, UninstallAssembly, UninstallAssembly method [Side-by-side Assemblies], UninstallAssembly method [Side-by-side Assemblies],IAssemblyCache interface, setup.iassemblycache_uninstallassembly, winsxs/IAssemblyCache::UninstallAssembly
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
 - IAssemblyCache::UninstallAssembly
 - winsxs/IAssemblyCache::UninstallAssembly
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
 - IAssemblyCache.UninstallAssembly
---

# IAssemblyCache::UninstallAssembly


## -description

The <b>UnistallAssembly</b> method removes an application reference to an assembly from the side-by-side store. If there are no other references to the assembly by other applications, the assembly becomes unusable. Windows may remove the assembly's files from the side-by-side store and reclaim disk space at a later time.

## -parameters

### -param dwFlags [in]

This parameter must be 0.

### -param pszAssemblyName [in]

A pointer to a null-terminated string value that contains the fully-specified strong name of the assembly. If the full name is not provided, the result is undefined.

### -param pRefData [in]

A pointer to a <a href="/windows/win32/api/winsxs/ns-winsxs-fusion_install_reference">FUSION_INSTALL_REFERENCE</a> structure that describes the application that holds the reference to the assembly being removed. If this value is null, no  references to the assembly by applications  are left in the side-by-side store and the assembly's files are removed.

<div class="alert"><b>Note</b>  The characters \, /, :, ;, *, &lt;, &gt;, and | are invalid in the reference ID.</div>
<div> </div>

### -param pulDisposition [out, optional]

A pointer to an integer value that describes the action performed.


The <i>pulDisposition</i> parameter can contain one of the following values or null.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_UNINSTALL_DISPOSITION_UNINSTALLED"></a><a id="iassemblycache_uninstall_disposition_uninstalled"></a><dl>
<dt><b>IASSEMBLYCACHE_UNINSTALL_DISPOSITION_UNINSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The assembly files have been removed from the side-by-side store.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_UNINSTALL_DISPOSITION_STILL_IN_USE"></a><a id="iassemblycache_uninstall_disposition_still_in_use"></a><dl>
<dt><b>IASSEMBLYCACHE_UNINSTALL_DISPOSITION_STILL_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The assembly's files have not been removed because an application is using the assembly.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_UNINSTALL_DISPOSITION_ALREADY_UNINSTALLED"></a><a id="iassemblycache_uninstall_disposition_already_uninstalled"></a><dl>
<dt><b>IASSEMBLYCACHE_UNINSTALL_DISPOSITION_ALREADY_UNINSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The assembly does not exist in the side-by-side store.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_UNINSTALL_DISPOSITION_DELETE_PENDING"></a><a id="iassemblycache_uninstall_disposition_delete_pending"></a><dl>
<dt><b>IASSEMBLYCACHE_UNINSTALL_DISPOSITION_DELETE_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_UNINSTALL_DISPOSITION_HAS_INSTALL_REFERENCES"></a><a id="iassemblycache_uninstall_disposition_has_install_references"></a><dl>
<dt><b>IASSEMBLYCACHE_UNINSTALL_DISPOSITION_HAS_INSTALL_REFERENCES</b></dt>
</dl>
</td>
<td width="60%">
The assembly's files have not been removed because the side-by-side store contains a reference to the assembly by another application.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_UNINSTALL_DISPOSITION_REFERENCE_NOT_FOUND"></a><a id="iassemblycache_uninstall_disposition_reference_not_found"></a><dl>
<dt><b>IASSEMBLYCACHE_UNINSTALL_DISPOSITION_REFERENCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The reference specified in <i>pRefData</i> does not exist in the side-by-side store.

</td>
</tr>
</table>

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
The files of the assembly have been removed from the side-by-side store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The operation succeeded and the reference to the assembly was removed. The assembly files were not removed from the side-by-side store for the reason described by the value returned by <i>pulDisposition</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblycache">IAssemblyCache</a>