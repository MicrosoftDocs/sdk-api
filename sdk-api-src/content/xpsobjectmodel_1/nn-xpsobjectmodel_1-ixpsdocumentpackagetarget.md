---
UID: NN:xpsobjectmodel_1.IXpsDocumentPackageTarget
title: IXpsDocumentPackageTarget (xpsobjectmodel_1.h)
author: windows-sdk-content
description: The IXpsDocumentPackageTarget interface contains the elements needed for printing XPS content in the Document Printing model.
old-location: xps\ixpsdocumentpackagetarget.htm
tech.root: printdocs
ms.assetid: B8B43CE5-2222-428B-8E78-C7049D027EE1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsDocumentPackageTarget, IXpsDocumentPackageTarget interface [XPS Documents and Packaging], IXpsDocumentPackageTarget interface [XPS Documents and Packaging],described, xps.ixpsdocumentpackagetarget, xpsobjectmodel_1/IXpsDocumentPackageTarget
ms.topic: interface
f1_keywords: ["xpsobjectmodel_1/IXpsDocumentPackageTarget"]
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Xpsobjectmodel_1.idl
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
 - Xpsobjectmodel_1.h
api_name:
 - IXpsDocumentPackageTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsDocumentPackageTarget interface


## -description


The <b>IXpsDocumentPackageTarget</b> interface contains the elements needed for printing XPS content in the Document Printing model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsDocumentPackageTarget</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsDocumentPackageTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsDocumentPackageTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsdocumentpackagetarget-getxpsomfactory">GetXpsOMFactory</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsdocumentpackagetarget-getxpsompackagewriter">GetXpsOMPackageWriter</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsdocumentpackagetarget-getxpstype">GetXpsType</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-__midl___midl_itf_xpsobjectmodel_1_0000_0000_0001">XPS_DOCUMENT_TYPE</a> enumerated value for the document package.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory">IPrintDocumentPackageTargetFactory</a>



<a href="https://docs.microsoft.com/uwp/api/windows.graphics.printing.printmanager">Windows.Graphics.Printing.PrintManager</a>
 

 

