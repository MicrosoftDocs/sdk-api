---
UID: NF:winsxs.IAssemblyName.Clone
title: IAssemblyName::Clone (winsxs.h)
author: windows-sdk-content
description: The Clone method copies the current side-by-side assembly name to a new instance of IAssemblyName.
old-location: setup\iassemblyname_clone.htm
tech.root: SbsCs
ms.assetid: 5096b7de-e53d-49fa-bb43-16d768787b4e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Side-by-side Assemblies], Clone method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],Clone method, IAssemblyName.Clone, IAssemblyName::Clone, setup.iassemblyname_clone, winsxs/IAssemblyName::Clone
ms.topic: method
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
 - IAssemblyName.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssemblyName::Clone


## -description


The <b>Clone</b> method copies the  current side-by-side assembly name to a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a>.


## -parameters




### -param pName [out]

Pointer to the location that contains the pointer to the new instance of <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a>
 

 

