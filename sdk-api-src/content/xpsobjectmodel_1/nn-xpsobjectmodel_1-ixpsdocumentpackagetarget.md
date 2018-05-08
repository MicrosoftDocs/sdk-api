---
UID: NN:xpsobjectmodel_1.IXpsDocumentPackageTarget
title: IXpsDocumentPackageTarget
author: windows-driver-content
description: The IXpsDocumentPackageTarget interface contains the elements needed for printing XPS content in the Document Printing model.
old-location: xps\ixpsdocumentpackagetarget.htm
old-project: printdocs
ms.assetid: B8B43CE5-2222-428B-8E78-C7049D027EE1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsDocumentPackageTarget, IXpsDocumentPackageTarget interface [XPS Documents and Packaging], IXpsDocumentPackageTarget interface [XPS Documents and Packaging],described, xps.ixpsdocumentpackagetarget, xpsobjectmodel_1/IXpsDocumentPackageTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Xpsobjectmodel_1.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_DOCUMENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xpsobjectmodel_1.h
api_name:
-	IXpsDocumentPackageTarget
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsDocumentPackageTarget interface


## -description


The <b>IXpsDocumentPackageTarget</b> interface contains the elements needed for printing XPS content in the Document Printing model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsDocumentPackageTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsDocumentPackageTarget</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/130114DF-DEE7-4ADD-8080-7D804F9F296E">GetXpsOMFactory</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D20AE05F-466F-44B6-972A-06AA872FF7BA">GetXpsOMPackageWriter</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A2B2523F-2F07-4331-A8EA-84BB6636B948">GetXpsType</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/C34629CB-7F8C-4126-BBE3-BF506D7586E9">XPS_DOCUMENT_TYPE</a> enumerated value for the document package.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/631FBF5E-1DDF-49A9-8E1E-201BC6996EA5">IPrintDocumentPackageTargetFactory</a>



<a href="http://msdn.microsoft.com/en-us/library/windows/apps/windows.graphics.printing.printmanager.aspx">Windows.Graphics.Printing.PrintManager</a>
 

 

