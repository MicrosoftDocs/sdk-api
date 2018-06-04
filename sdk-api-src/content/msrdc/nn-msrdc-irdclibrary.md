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

# IRdcLibrary interface


## -description


The <b>IRdcLibrary</b> interface is the primary interface 
    for using RDC.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcLibrary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRdcLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b42c7b46-9f3c-46d2-a6a7-b5176fc40645">ComputeDefaultRecursionDepth</a>
</td>
<td align="left" width="63%">
Computes the maximum level of recursion for the specified file size.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21e83ed0-974a-470f-8a7f-1776f1575100">CreateComparator</a>
</td>
<td align="left" width="63%">
Creates a signature comparator. The caller must create a separate signature comparator for each 
    level of recursion.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cd64c3f-acd7-4e59-916f-90e90f452e12">CreateGenerator</a>
</td>
<td align="left" width="63%">
Creates a signature generator that will generate the specified levels of 
     signatures.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a39e26bc-7493-4def-af6d-cf3620ec8a9f">CreateGeneratorParameters</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> 
     interface pointer initialized with the  parameters necessary for a signature generator.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08627c9d-7470-47ab-9209-32734082c393">CreateSignatureReader</a>
</td>
<td align="left" width="63%">
Creates a signature reader to allow an application to decode the contents of a signature 
     file.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eef00e8-62d9-49bc-8340-fb56f5a4573d">GetRDCVersion</a>
</td>
<td align="left" width="63%">
Returns the version of the installed RDC runtime and the oldest version of the RDC interfaces 
     supported by the installed runtime.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fbced31-a230-44d4-a9ee-bb3e15df2563">OpenGeneratorParameters</a>
</td>
<td align="left" width="63%">
Opens an existing serialized parameter block and returns an 
     <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointer 
     initialized with the data.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/a3131654-e849-4a88-acec-c49a61653bad">Remote Differential Compression Interfaces</a>
 

 

