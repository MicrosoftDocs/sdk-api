---
UID: NN:xpsobjectmodel_2.IXpsDocumentPackageTarget3D
title: IXpsDocumentPackageTarget3D
author: windows-sdk-content
description: Provides methods for sending 3D content to XPS for printing.
old-location: xps\ixpsdocumentpackagetarget3d.htm
old-project: printdocs
ms.assetid: 7273235D-EB74-4FB2-B471-FCFF71741BF6
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsDocumentPackageTarget3D, IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging], IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging],described, xps.ixpsdocumentpackagetarget3d, xpsobjectmodel_2/IXpsDocumentPackageTarget3D
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_1.idl; XpsObjectModel_2.idl
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
-	XpsObjectModel_2.h
api_name:
-	IXpsDocumentPackageTarget3D
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsDocumentPackageTarget3D interface


## -description


Provides methods for sending 3D content to XPS for printing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsDocumentPackageTarget3D</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsDocumentPackageTarget3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsDocumentPackageTarget3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A96555FB-9312-46E3-A347-A726A2C39BFC">GetXpsOMFactory</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F3A6997-B325-4406-A731-5C2EAD875125">GetXpsOMPackageWriter3D</a>
</td>
<td align="left" width="63%">
Gets a new <a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a> object for the document package.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/B8B43CE5-2222-428B-8E78-C7049D027EE1">IXpsDocumentPackageTarget</a>



<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>



<a href="https://msdn.microsoft.com/F5A13938-FC6A-4158-BC39-43F7ACF7D406">Supporting 3D printing</a>
 

 

