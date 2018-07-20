---
UID: NN:docobj.IPrint
title: IPrint
author: windows-sdk-content
description: Enables compound documents in general and active documents in particular to support programmatic printing.
old-location: com\iprint.htm
old-project: com
ms.assetid: eb0d15c0-8a34-4211-b840-29d5862cf767
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IPrint, IPrint interface [COM], IPrint interface [COM],described, _ctrl_iprint, com.iprint, docobj/IPrint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DOCMISC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IPrint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPrint interface


## -description


Enables compound documents in general and active documents in particular to support programmatic printing. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrint</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IPrint</b> also has these types of members:
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



