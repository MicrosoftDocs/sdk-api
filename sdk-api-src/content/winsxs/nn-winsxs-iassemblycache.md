---
UID: NN:winsxs.IAssemblyCache
title: IAssemblyCache (winsxs.h)
author: windows-sdk-content
description: The IAssemblyCache interface can be used to install, uninstall, or query a side-by-side assembly. An instance of IAssemblyCache is obtained by calling the CreateAssemblyCache function.
old-location: setup\iassemblycache.htm
tech.root: SbsCs
ms.assetid: 6c411ae7-5a8f-47ca-a9c1-e23000f64620
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAssemblyCache, IAssemblyCache interface [Side-by-side Assemblies], IAssemblyCache interface [Side-by-side Assemblies],described, setup.iassemblycache, winsxs/IAssemblyCache
ms.topic: interface
f1_keywords: ["winsxs/IAssemblyCache"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sxs.dll
api_name:
 - IAssemblyCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssemblyCache interface


## -description


The <b>IAssemblyCache</b> interface can be used to install, uninstall, or query a side-by-side assembly. An instance of <b>IAssemblyCache</b> is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-createassemblycache">CreateAssemblyCache</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssemblyCache</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAssemblyCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssemblyCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-createassemblycacheitem">CreateAssemblyCacheItem</a>
</td>
<td align="left" width="63%">
Adds an item to the assembly cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-installassembly">InstallAssembly</a>
</td>
<td align="left" width="63%">
Adds an application reference to an assembly and copies the files of the assembly to the side-by-side store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-queryassemblyinfo">QueryAssemblyInfo</a>
</td>
<td align="left" width="63%">
Queries for assembly information and validates the files in the side-by-side assembly store against the assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-uninstallassembly">UninstallAssembly</a>
</td>
<td align="left" width="63%">
Removes an application reference to an assembly from the side-by-side store. Removes the assembly's files if there are no other references to the assembly by other applications.

</td>
</tr>
</table> 

