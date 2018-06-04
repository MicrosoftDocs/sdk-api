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

A pointer to a <a href="https://msdn.microsoft.com/daa2b625-1522-4239-9c62-65f09b50f74c">FUSION_INSTALL_REFERENCE</a> structure that describes the application that holds the reference to the assembly being installed. If this parameter is null, the assembly files are copied, but no application reference is added to the side-by-side store.


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




<a href="https://msdn.microsoft.com/6c411ae7-5a8f-47ca-a9c1-e23000f64620">IAssemblyCache</a>
 

 

