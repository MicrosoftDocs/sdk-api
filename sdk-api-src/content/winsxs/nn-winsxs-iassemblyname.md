---
UID: NN:winsxs.IAssemblyName
title: IAssemblyName (winsxs.h)
author: windows-sdk-content
description: The IAssemblyName interface represents a side-by-side assembly name.
old-location: setup\iassemblyname.htm
tech.root: SbsCs
ms.assetid: 304b8fb3-5d17-4af0-b070-450a40dc5cc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAssemblyName, IAssemblyName interface [Side-by-side Assemblies], IAssemblyName interface [Side-by-side Assemblies],described, setup.iassemblyname, winsxs/IAssemblyName
ms.topic: interface
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
 - IAssemblyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssemblyName interface


## -description


The <b>IAssemblyName</b> interface represents a side-by-side assembly name. The side-by-side assembly name consists of a set of name-value pairs that describe the side-by-side assembly. An instance of the <b>IAssemblyName</b> interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-createassemblynameobject">CreateAssemblyNameObject</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssemblyName</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAssemblyName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssemblyName</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-clone">Clone</a>
</td>
<td align="left" width="63%">
Copies the  current side-by-side assembly name to a new instance of <b>IAssemblyName</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-finalize">Finalize</a>
</td>
<td align="left" width="63%">
Prevents a side-by-side assembly name from being changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Gets a string representation of the side-by-side assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getname">GetName</a>
</td>
<td align="left" width="63%">
Returns the name portion of the assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of a name-value pair in the assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Compares the current assembly name to another assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Adds or changes a name-value pair of the assembly name.

</td>
</tr>
</table> 

