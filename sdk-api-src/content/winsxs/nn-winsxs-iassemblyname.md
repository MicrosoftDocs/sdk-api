---
UID: NN:winsxs.IAssemblyName
title: IAssemblyName
author: windows-sdk-content
description: The IAssemblyName interface represents a side-by-side assembly name.
old-location: setup\iassemblyname.htm
old-project: sbscs
ms.assetid: 304b8fb3-5d17-4af0-b070-450a40dc5cc9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IAssemblyName, IAssemblyName interface [Side-by-side Assemblies], IAssemblyName interface [Side-by-side Assemblies],described, setup.iassemblyname, winsxs/IAssemblyName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsxs.h
req.include-header: 
req.redist: 
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
 - IAssemblyName
product: Windows
targetos: Windows
req.lib: 
req.dll: Sxs.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAssemblyName interface


## -description


The <b>IAssemblyName</b> interface represents a side-by-side assembly name. The side-by-side assembly name consists of a set of name-value pairs that describe the side-by-side assembly. An instance of the <b>IAssemblyName</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssemblyName</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAssemblyName</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5096b7de-e53d-49fa-bb43-16d768787b4e">Clone</a>
</td>
<td align="left" width="63%">
Copies the  current side-by-side assembly name to a new instance of <b>IAssemblyName</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9930826e-3082-4ad3-991e-13cf426983a4">Finalize</a>
</td>
<td align="left" width="63%">
Prevents a side-by-side assembly name from being changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2d74d67-a893-4f2f-8161-80bf3d5cbedb">GetDisplayName</a>
</td>
<td align="left" width="63%">
Gets a string representation of the side-by-side assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b27ebe4e-02b6-473f-a8cb-c68a3e65e493">GetName</a>
</td>
<td align="left" width="63%">
Returns the name portion of the assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0526fac9-1a3f-403b-b886-a7f833913e18">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of a name-value pair in the assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/798102ce-b696-4940-941d-c3fd3054c584">IsEqual</a>
</td>
<td align="left" width="63%">
Compares the current assembly name to another assembly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057bc5b3-008b-495b-b96c-2c0dcc43f1a4">SetProperty</a>
</td>
<td align="left" width="63%">
Adds or changes a name-value pair of the assembly name.

</td>
</tr>
</table> 

