---
UID: NN:documenttarget.IPrintDocumentPackageTarget
title: IPrintDocumentPackageTarget
author: windows-sdk-content
description: Allows users to enumerate the supported package target types and to create one with a given type ID. IPrintDocumentPackageTarget also supports the tracking of the package printing progress and cancelling.
old-location: xps\iprintdocumentpackagetarget.htm
old-project: printdocs
ms.assetid: 0F63C626-DB58-4952-BBB3-7E3901429C35
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IPrintDocumentPackageTarget, IPrintDocumentPackageTarget interface [XPS Documents and Packaging], IPrintDocumentPackageTarget interface [XPS Documents and Packaging],described, documenttarget/IPrintDocumentPackageTarget, xps.iprintdocumentpackagetarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: PrintDocumentPackageCompletion
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - documenttarget.h
api_name:
 - IPrintDocumentPackageTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPrintDocumentPackageTarget interface


## -description


Allows users to enumerate the supported package target types and to create one with a given type ID. <b>IPrintDocumentPackageTarget</b> also supports the tracking of the package printing progress and cancelling.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintDocumentPackageTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintDocumentPackageTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintDocumentPackageTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the current print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7D9A749D-954E-43BA-A522-98CBAD79D18C">GetPackageTarget</a>
</td>
<td align="left" width="63%">
Retrieves the pointer to the specific document package target, which allows the client to add a document with the given target type. Clients can call this method multiple times but they always have to use  the same target ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2875B751-0D49-4CFC-AF96-7009400E5D6E">GetPackageTargetTypes</a>
</td>
<td align="left" width="63%">
Enumerates the supported target types.

</td>
</tr>
</table> 

