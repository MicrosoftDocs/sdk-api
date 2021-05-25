---
UID: NF:rometadataapi.IMetaDataAssemblyImport.FindAssembliesByName
title: IMetaDataAssemblyImport::FindAssembliesByName (rometadataapi.h)
description: Gets an array of assemblies with the specified name, using the standard rules employed by the common language runtime (CLR) for resolving references.
helpviewer_keywords: ["FindAssembliesByName","FindAssembliesByName method [Windows Runtime]","FindAssembliesByName method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","FindAssembliesByName method","IMetaDataAssemblyImport.FindAssembliesByName","IMetaDataAssemblyImport::FindAssembliesByName","rometadataapi/IMetaDataAssemblyImport::FindAssembliesByName","winrt.imetadataassemblyimport_findassembliesbyname"]
old-location: winrt\imetadataassemblyimport_findassembliesbyname.htm
tech.root: WinRT
ms.assetid: 147158ba-060e-404e-9721-3d0c2498f5c9
ms.date: 12/05/2018
ms.keywords: FindAssembliesByName, FindAssembliesByName method [Windows Runtime], FindAssembliesByName method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],FindAssembliesByName method, IMetaDataAssemblyImport.FindAssembliesByName, IMetaDataAssemblyImport::FindAssembliesByName, rometadataapi/IMetaDataAssemblyImport::FindAssembliesByName, winrt.imetadataassemblyimport_findassembliesbyname
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMetaDataAssemblyImport::FindAssembliesByName
 - rometadataapi/IMetaDataAssemblyImport::FindAssembliesByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport.FindAssembliesByName
---

# IMetaDataAssemblyImport::FindAssembliesByName


## -description

Gets an array of assemblies with the specified name, using the standard rules employed by the common language runtime (CLR) for resolving references.

## -parameters

### -param szAppBase [in]

The root directory in which to search for the given assembly. If this value is set to null, <b>FindAssembliesByName</b> will look only in the global assembly cache for the assembly.

### -param szPrivateBin [in]

A list of semicolon-delimited subdirectories (for example, "bin;bin2"), under the root directory, in which to search for the assembly. These directories are probed in addition to those specified in the default probing rules.

### -param szAssemblyName [in]

The name of the assembly to find. The format of this string is defined in the class reference page for <a href="/dotnet/api/system.reflection.assemblyname">AssemblyName</a>.

### -param ppIUnk [out]

An array of type IUnknown in which to put the <a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetadataAssemblyImport</a> interface pointers.

### -param cMax [in]

The maximum number of interface pointers that can be placed in <i>ppIUnk</i>.

### -param pcAssemblies [out]

The number of interface pointers returned. That is, the number of interface pointers actually placed in <i>ppIUnk</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>FindAssembliesByName</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no assemblies.</td>
</tr>
</table>

## -remarks

Given an assembly name, the <b>FindAssembliesByName</b> method finds the assembly by following the standard rules for resolving assembly references. <b>FindAssembliesByName</b> allows the caller to configure various aspects of the assembly resolver context, such as application base and private search path.

<b>FindAssembliesByName</b> returns an <a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a> pointer to the file containing the assembly manifest for the assembly name that is passed in. If the given assembly name is not fully specified (for example, if it does not include a version), multiple assemblies might be returned.

<b>FindAssembliesByName</b> is commonly used by a compiler that attempts to find a referenced assembly at compile time.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>