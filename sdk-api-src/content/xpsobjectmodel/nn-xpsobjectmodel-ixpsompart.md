---
UID: NN:xpsobjectmodel.IXpsOMPart
title: IXpsOMPart (xpsobjectmodel.h)
author: windows-sdk-content
description: The base interface for all XPS document part interfaces.
old-location: xps\ixpsompart.htm
tech.root: printdocs
ms.assetid: 71cd0155-6c95-42ca-bfc3-dffd43d95dc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPart, IXpsOMPart interface [XPS Documents and Packaging], IXpsOMPart interface [XPS Documents and Packaging],described, xps.ixpsompart, xpsobjectmodel/IXpsOMPart
ms.topic: interface
f1_keywords: 
 - "xpsobjectmodel/IXpsOMPart"
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - IXpsOMPart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPart interface


## -description


The base interface for all XPS document part interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPart</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMPart</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPart</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompart-getpartname">GetPartName</a>
</td>
<td align="left" width="63%">
Gets the name that will be used when the part is serialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompart-setpartname">SetPartName</a>
</td>
<td align="left" width="63%">
Sets the name that will be used when the part is serialized.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

