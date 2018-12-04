---
UID: NN:mergemod.IMsmError
title: IMsmError
author: windows-sdk-content
description: The IMsmError interface retrieves details about a single merge error.
old-location: setup\imsmerror_interface.htm
tech.root: msi
ms.assetid: 705f53ca-82f4-4929-b2a3-0ace8e4ca19b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMsmError, IMsmError interface, IMsmError interface,described, mergemod/IMsmError, setup.imsmerror_interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmError
 - IMsmError.get_Type
 - IMsmError.get_Path
 - IMsmError.get_Language
 - IMsmError.get_DatabaseTable
 - IMsmError.get_DatabaseKeys
 - IMsmError.get_ModuleTable
 - IMsmError.get_ModuleKeys
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmError interface


## -description


The <b>IMsmError</b> interface retrieves details about a single merge error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmError</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMsmError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_DatabaseKeys</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/416a6cef-4c70-4c06-a8d2-801c9440e25a">DatabaseKeys</a> property of the <a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_DatabaseTable</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/38ff45ca-4bd6-43f3-88ad-db4077daeb77">DatabaseTable</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Language</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/9b0608d1-b6e8-4cf9-8119-3c2909156516">Language</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_ModuleKeys</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/b02b609b-4682-4228-b29a-364f079e863c">ModuleKeys</a> property of the <a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_ModuleTable</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Path</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b">Path</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Type</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

