---
UID: NS:winsxs._ASSEMBLY_INFO
title: ASSEMBLY_INFO (winsxs.h)
description: The ASSEMBLY_INFO structure contains information about an assembly in the side-by-side assembly store. The information is used by the QueryAssemblyInfo method.
helpviewer_keywords: ["ASSEMBLYINFO_FLAG_INSTALLED","ASSEMBLY_INFO","ASSEMBLY_INFO structure [Side-by-side Assemblies]","setup.assembly_info_","winsxs/ASSEMBLY_INFO"]
old-location: setup\assembly_info_.htm
tech.root: setup
ms.assetid: 4281b375-0edd-453b-9505-e7dc5bd586fc
ms.date: 12/05/2018
ms.keywords: ASSEMBLYINFO_FLAG_INSTALLED, ASSEMBLY_INFO, ASSEMBLY_INFO structure [Side-by-side Assemblies], setup.assembly_info_, winsxs/ASSEMBLY_INFO
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ASSEMBLY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASSEMBLY_INFO
 - winsxs/_ASSEMBLY_INFO
 - ASSEMBLY_INFO
 - winsxs/ASSEMBLY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsxs.h
api_name:
 - ASSEMBLY_INFO
---

# ASSEMBLY_INFO structure


## -description

The <b>ASSEMBLY_INFO</b> structure contains information about an assembly in the side-by-side assembly store.  The information is used by the <a href="/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-queryassemblyinfo">QueryAssemblyInfo</a> method.

## -struct-fields

### -field cbAssemblyInfo

The size of the structure in bytes.

### -field dwAssemblyFlags

 This member can contain the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ASSEMBLYINFO_FLAG_INSTALLED"></a><a id="assemblyinfo_flag_installed"></a><dl>
<dt><b>ASSEMBLYINFO_FLAG_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Set this flag when using Windows Vista and later or Windows Server 2008 and later with the assembly installed in the side-by-side assembly store.

</td>
</tr>
</table>

### -field uliAssemblySizeInKB

The size of the files that comprise the assembly in kilobytes (KB).

### -field pszCurrentAssemblyPathBuf

A pointer to a null-terminated string that contains the path to the manifest file.

### -field cchBuf

The number  of characters, including the null terminator, in the string specified by <i>pszCurrentAssemblyPathBuf</i>.