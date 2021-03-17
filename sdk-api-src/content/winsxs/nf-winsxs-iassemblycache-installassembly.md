---
UID: NF:winsxs.IAssemblyCache.InstallAssembly
title: IAssemblyCache::InstallAssembly (winsxs.h)
description: The InstallAssembly method adds an application reference to an assembly to the side-by-side store and copies the files of the assembly to the side-by-side store. The files of the assembly being installed must be present in the current file system.
helpviewer_keywords: ["IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH","IASSEMBLYCACHE_INSTALL_FLAG_REFRESH","IAssemblyCache interface [Side-by-side Assemblies]","InstallAssembly method","IAssemblyCache.InstallAssembly","IAssemblyCache::InstallAssembly","InstallAssembly","InstallAssembly method [Side-by-side Assemblies]","InstallAssembly method [Side-by-side Assemblies]","IAssemblyCache interface","setup.iassemblycache_installassembly","winsxs/IAssemblyCache::InstallAssembly"]
old-location: setup\iassemblycache_installassembly.htm
tech.root: setup
ms.assetid: aff1da20-9e82-43d5-b601-f73ee2dba0fe
ms.date: 12/05/2018
ms.keywords: IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH, IASSEMBLYCACHE_INSTALL_FLAG_REFRESH, IAssemblyCache interface [Side-by-side Assemblies],InstallAssembly method, IAssemblyCache.InstallAssembly, IAssemblyCache::InstallAssembly, InstallAssembly, InstallAssembly method [Side-by-side Assemblies], InstallAssembly method [Side-by-side Assemblies],IAssemblyCache interface, setup.iassemblycache_installassembly, winsxs/IAssemblyCache::InstallAssembly
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
 - IAssemblyCache::InstallAssembly
 - winsxs/IAssemblyCache::InstallAssembly
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
 - IAssemblyCache.InstallAssembly
---

# IAssemblyCache::InstallAssembly


## -description

The <b>InstallAssembly</b> method adds an application reference to an assembly to the side-by-side store and copies the files of the assembly to the side-by-side store. The files of the assembly being installed must be present in the current file system.

## -parameters

### -param dwFlags [in]

This parameter specifies how existing files in the side-by-side store are to replaced by files in the assembly being installed.


One of the following options can be specified.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_INSTALL_FLAG_REFRESH"></a><a id="iassemblycache_install_flag_refresh"></a><dl>
<dt><b>IASSEMBLYCACHE_INSTALL_FLAG_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Replace existing files in the side-by-side store with the files in the assembly being installed if the version of the file in the assembly is greater than or equal to the version of the existing file.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH"></a><a id="iassemblycache_install_flag_force_refresh"></a><dl>
<dt><b>IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Replace existing files in the side-by-side store with the files in the assembly being installed.

</td>
</tr>
</table>

### -param pszManifestFilePath [in]

A pointer to a string value that contains the full path to the dynamic-linked library (DLL) or executable (EXE) file that contains the assembly manifest. Any other assembly files must be located in the same directory as this DLL or EXE.

### -param pRefData [in, optional]

A pointer to a <a href="/windows/win32/api/winsxs/ns-winsxs-fusion_install_reference">FUSION_INSTALL_REFERENCE</a> structure that describes the application that holds the reference to the assembly being installed. If this parameter is null, the assembly files are copied, but no application reference is added to the side-by-side store.

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