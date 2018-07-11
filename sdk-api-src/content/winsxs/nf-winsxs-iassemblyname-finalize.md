---
UID: NF:winsxs.IAssemblyName.Finalize
title: IAssemblyName::Finalize
author: windows-sdk-content
description: The Finalize method prevents a side-by-side assembly name from being changed. After Finalize is called, additional calls to the SetProperty returns E_UNEXPECTED.
old-location: setup\iassemblyname_finalize.htm
old-project: sbscs
ms.assetid: 9930826e-3082-4ad3-991e-13cf426983a4
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: Finalize, Finalize method [Side-by-side Assemblies], Finalize method [Side-by-side Assemblies],IAssemblyName interface, IAssemblyName interface [Side-by-side Assemblies],Finalize method, IAssemblyName.Finalize, IAssemblyName::Finalize, setup.iassemblyname_finalize, winsxs/IAssemblyName::Finalize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CREATE_ASM_NAME_OBJ_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sxs.dll
api_name:
 - IAssemblyName.Finalize
product: Windows
targetos: Windows
req.lib: 
req.dll: Sxs.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAssemblyName::Finalize


## -description


The <b>Finalize</b> method prevents a side-by-side  assembly name from being changed. After <b>Finalize</b> is called, additional calls to the <a href="https://msdn.microsoft.com/057bc5b3-008b-495b-b96c-2c0dcc43f1a4">SetProperty</a> returns <b>E_UNEXPECTED</b>.


## -parameters






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




<a href="https://msdn.microsoft.com/304b8fb3-5d17-4af0-b070-450a40dc5cc9">IAssemblyName</a>
 

 

