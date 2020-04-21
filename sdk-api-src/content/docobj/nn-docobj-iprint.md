---
UID: NN:docobj.IPrint
title: IPrint (docobj.h)
description: Enables compound documents in general and active documents in particular to support programmatic printing.helpviewer_keywords: ["IPrint","IPrint interface [COM]","IPrint interface [COM]","described","_ctrl_iprint","com.iprint","docobj/IPrint"]
old-location: com\iprint.htm
tech.root: com
ms.assetid: eb0d15c0-8a34-4211-b840-29d5862cf767
ms.date: 12/05/2018
ms.keywords: IPrint, IPrint interface [COM], IPrint interface [COM],described, _ctrl_iprint, com.iprint, docobj/IPrint
f1_keywords:
- docobj/IPrint
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DocObj.h
api_name:
- IPrint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPrint interface


## -description


Enables compound documents in general and active documents in particular to support programmatic printing. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrint</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrint</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iprint-getpageinfo">GetPageInfo</a>
</td>
<td align="left" width="63%">
Retrieves the number of a document's first page and the total number of pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iprint-print">Print</a>
</td>
<td align="left" width="63%">
Prints an object on the specified printer, using the specified job requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iprint-setinitialpagenum">SetInitialPageNum</a>
</td>
<td align="left" width="63%">
Sets the page number of the first page of a document.

</td>
</tr>
</table> 


## -remarks



After a document is loaded, containers and other clients can call <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iprint-print">IPrint::Print</a> to instruct a document to print itself, specifying printing control flags, the target device, the particular pages to print, and other options. The client can control the continuation of printing by calling the <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-icontinuecallback">IContinueCallback</a> interface. 


An object that implements <b>IPrint</b> registers itself with the <b>Printable</b> key stored under its CLSID as follows:


<b>HKEY_CLASSES_ROOT\CLSID\{...}\Printable</b>



Callers determine whether a particular object class supports programmatic printing of its persistent state by looking in the registry for this key.



