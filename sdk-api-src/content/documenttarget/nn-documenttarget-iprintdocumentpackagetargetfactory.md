---
UID: NN:documenttarget.IPrintDocumentPackageTargetFactory
title: IPrintDocumentPackageTargetFactory
author: windows-sdk-content
description: Used with IPrintDocumentPackageTarget for starting a print job.
old-location: xps\iprintdocumentpackagetargetfactory.htm
tech.root: printdocs
ms.assetid: 631FBF5E-1DDF-49A9-8E1E-201BC6996EA5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPrintDocumentPackageTargetFactory, IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging], IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging],described, documenttarget/IPrintDocumentPackageTargetFactory, xps.iprintdocumentpackagetargetfactory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - documenttarget.h
api_name:
 - IPrintDocumentPackageTargetFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDocumentPackageTargetFactory interface


## -description


Used with <a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a> for starting a print job.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintDocumentPackageTargetFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintDocumentPackageTargetFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintDocumentPackageTargetFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F611305F-B577-403F-AD8A-402ABE8F6768">CreateDocumentPackageTargetForPrintJob</a>
</td>
<td align="left" width="63%">
Acts as the entry point for creating an <a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a> object.

</td>
</tr>
</table> 

