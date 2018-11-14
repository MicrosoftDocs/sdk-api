---
UID: NN:xpsobjectmodel_1.IXpsOMPackage1
title: IXpsOMPackage1
author: windows-sdk-content
description: Inherits from IXpsOMPackage.
old-location: xps\ixpsompackage1.htm
tech.root: printdocs
ms.assetid: 455b7f0b-ade4-4e00-bd9d-836335a7982e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMPackage1, IXpsOMPackage1 interface [XPS Documents and Packaging], IXpsOMPackage1 interface [XPS Documents and Packaging],described, xps.ixpsompackage1, xpsobjectmodel_1/IXpsOMPackage1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - none
 - none.dll
api_name:
 - IXpsOMPackage1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackage1 interface


## -description


Inherits from IXpsOMPackage. 

Provides support for:

Detecting the format/type of an XPS package loaded in the XPS OM.

Saving an in-memory XPS OM package to an MSXPS or OpenXPS package byte stream or file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPackage1</b> interface inherits from <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>. <b>IXpsOMPackage1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPackage1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f51e5c5-ac80-4f45-a0bb-ef19137fe391">IXpsOMPackage1::GetDocumentType</a>
</td>
<td align="left" width="63%">
Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">XPS Documents</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/524f951f-5a2b-4ed1-8435-4426739d38f8">IXpsOMPackage1::WriteToFile1</a>
</td>
<td align="left" width="63%">
Writes an XPS OM to a file as an XPS package of a specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f430aa1-1570-44d6-9aec-a4b2fb55f2dc">IXpsOMPackage1::WriteToStream1</a>
</td>
<td align="left" width="63%">
Writes an XPS OM to a stream as an XPS package of a specified type.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
The base interface is defined and documented in Windows 7 SDK.

http://msdn.microsoft.com/en-us/library/dd372618(v=VS.85).aspx




## -see-also




<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>
 

 

