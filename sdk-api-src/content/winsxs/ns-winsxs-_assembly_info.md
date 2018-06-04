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

# _ASSEMBLY_INFO structure


## -description


The <b>ASSEMBLY_INFO</b> structure contains information about an assembly in the side-by-side assembly store.  The information is used by the <a href="https://msdn.microsoft.com/fc13e5ac-60cf-43f2-b50e-00be3a1ad270">QueryAssemblyInfo</a> method.


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

