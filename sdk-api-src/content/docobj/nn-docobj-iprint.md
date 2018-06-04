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

# IPrint interface


## -description


Enables compound documents in general and active documents in particular to support programmatic printing. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrint</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPrint</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrint</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f3a2d21-5345-4c4e-9928-37dcd6ec5fcc">GetPageInfo</a>
</td>
<td align="left" width="63%">
Retrieves the number of a document's first page and the total number of pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30554d89-ad80-4d73-b44a-97ae5079feb8">Print</a>
</td>
<td align="left" width="63%">
Prints an object on the specified printer, using the specified job requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/352a4dc0-c79e-46e3-8212-55fd7d2916bc">SetInitialPageNum</a>
</td>
<td align="left" width="63%">
Sets the page number of the first page of a document.

</td>
</tr>
</table> 


## -remarks



After a document is loaded, containers and other clients can call <a href="https://msdn.microsoft.com/30554d89-ad80-4d73-b44a-97ae5079feb8">IPrint::Print</a> to instruct a document to print itself, specifying printing control flags, the target device, the particular pages to print, and other options. The client can control the continuation of printing by calling the <a href="https://msdn.microsoft.com/55c960be-48e3-42e1-b459-49227be62171">IContinueCallback</a> interface. 


An object that implements <b>IPrint</b> registers itself with the <b>Printable</b> key stored under its CLSID as follows:


<b>HKEY_CLASSES_ROOT\CLSID\{...}\Printable</b>



Callers determine whether a particular object class supports programmatic printing of its persistent state by looking in the registry for this key.



