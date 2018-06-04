---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

The name of the assembly to find. The format of this string is defined in the class reference page for <a href="http://msdn.microsoft.com/en-us/library/system.reflection.assemblyname.aspx">AssemblyName</a>.


### -param ppIUnk [out]

An array of type IUnknown in which to put the <a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetadataAssemblyImport</a> interface pointers.


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
<td>There are no assembies.</td>
</tr>
</table>
 




## -remarks



Given an assembly name, the <b>FindAssembliesByName</b> method finds the assembly by following the standard rules for resolving assembly references. <b>FindAssembliesByName</b> allows the caller to configure various aspects of the assembly resolver context, such as application base and private search path.

<b>FindAssembliesByName</b> returns an <a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a> pointer to the file containing the assembly manifest for the assembly name that is passed in. If the given assembly name is not fully specified (for example, if it does not include a version), multiple assemblies might be returned.

<b>FindAssembliesByName</b> is commonly used by a compiler that attempts to find a referenced assembly at compile time.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

