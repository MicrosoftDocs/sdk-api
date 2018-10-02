---
UID: NN:xpsobjectmodel_1.IXpsOMObjectFactory1
title: IXpsOMObjectFactory1
author: windows-sdk-content
description: Inherits from IXpsOMObjectFactory.
old-location: xps\ixpsomobjectfactory1.htm
tech.root: printdocs
ms.assetid: f013e59d-83ae-453f-9cc5-9a8230729128
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMObjectFactory1, IXpsOMObjectFactory1 interface [XPS Documents and Packaging], IXpsOMObjectFactory1 interface [XPS Documents and Packaging],described, xps.ixpsomobjectfactory1, xpsobjectmodel_1/IXpsOMObjectFactory1
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMObjectFactory1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory1 interface


## -description


Inherits from IXpsOMObjectFactory. 

Adds support for:

Detecting the type of an XPS package. 

Loading of an OpenXPS packages into an XPS object model. 

Saving an in-memory XPS Object model to an OpenXPS package. 

Converting HDPhoto resources into JpegXR resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMObjectFactory1</b> interface inherits from <a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>. <b>IXpsOMObjectFactory1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMObjectFactory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07994e2b-b87b-49de-949d-eb7d771f0345">IXpsOMObjectFactory1::ConvertHDPhotoToJpegXR</a>
</td>
<td align="left" width="63%">
Converts an image resource from an HD Photo to a JpegXR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98cb0eca-229e-4224-bc9c-605f56cc298b">IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto</a>
</td>
<td align="left" width="63%">
Converts an image resource from a JpegXR to an HD Photo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5641576-9280-48a5-9fb6-ef3d2811386a">IXpsOMObjectFactory1::CreatePackageFromFile1</a>
</td>
<td align="left" width="63%">
Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9a7fd3a-d436-41b6-89ab-17baab9139e1">IXpsOMObjectFactory1::CreatePackageFromStream1</a>
</td>
<td align="left" width="63%">
Opens a stream that contains an XPS package and returns an instantiated XPS document object tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ad569a1-8b7a-473c-8bce-ad1fd843ec29">IXpsOMObjectFactory1::CreatePackageWriterOnFile1</a>
</td>
<td align="left" width="63%">
Opens a file for writing the contents of an XPS OM to an XPS package of a specified type. This method produces a package writer for either an MSXPS document or an OpenXPS document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce948f17-689a-4430-8152-20fbecaf6ee9">IXpsOMObjectFactory1::CreatePackageWriterOnStream1</a>
</td>
<td align="left" width="63%">
Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a400006-0f8f-4eb2-88c0-b559c6a4a0ba">IXpsOMObjectFactory1::CreatePageFromStream1</a>
</td>
<td align="left" width="63%">
Reads the page markup from the specified stream to create and populate an IXpsOMPage1 interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e69a139c-511c-43f3-86a3-22aab36f91fc">IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1</a>
</td>
<td align="left" width="63%">
Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface. The dictionary referenced by the dictionaryMarkupStream parameter can contain markup from either the OpenXPS or the MSXPS namespace. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a122c7cb-4166-46e1-a680-d0644ab8ce81">IXpsOMObjectFactory1::GetDocumentTypeFromFile</a>
</td>
<td align="left" width="63%">
Detects the type of XPS document that is stored in the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98d5bfc1-75f7-425f-b69d-11e74c15f08e">IXpsOMObjectFactory1::GetDocumentTypeFromStream</a>
</td>
<td align="left" width="63%">
Detects the type of XPS document that is stored in the specified stream.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
The base interface is defined and documented in Windows 7 SDK.

http://msdn.microsoft.com/en-us/library/dd372509(VS.85).aspx




## -see-also




<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>
 

 

